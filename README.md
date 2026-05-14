

Directory structure:
└── harsh09jt-StayCore/
    ├── AuthInGoService
    │   ├── app
    │   │   └── application.go
    │   ├── config
    │   │   ├── db
    │   │   │   └── db.go
    │   │   └── env
    │   │       └── env.go
    │   ├── controllers
    │   │   ├── permission.go
    │   │   ├── ping.go
    │   │   ├── role.go
    │   │   └── user.go
    │   ├── db
    │   │   ├── migrations
    │   │   │   ├── 20250721124056_create_users_table.sql
    │   │   │   ├── 20250729095851_create_role_table.sql
    │   │   │   ├── 20250729100519_create_permission_table.sql
    │   │   │   ├── 20250729101222_role_permission_table.sql
    │   │   │   └── 20250729102812_create_user_role.sql
    │   │   └── repositories
    │   │       ├── permission.go
    │   │       ├── role.go
    │   │       ├── role_permission.go
    │   │       ├── storage.go
    │   │       ├── user.go
    │   │       └── user_role.go
    │   ├── dtos
    │   │   ├── auth.go
    │   │   └── rbac.go
    │   ├── middlewares
    │   │   ├── auth.go
    │   │   ├── rate_limiter.go
    │   │   └── validator.go
    │   ├── models
    │   │   ├── rbac.go
    │   │   └── user.go
    │   ├── routers
    │   │   ├── permission_router.go
    │   │   ├── role_router.go
    │   │   ├── router.go
    │   │   └── user_router.go
    │   ├── services
    │   │   ├── permission_service.go
    │   │   ├── role_service.go
    │   │   └── user_service.go
    │   ├── utils
    │   │   ├── auth.go
    │   │   ├── json.go
    │   │   └── proxy.go
    │   ├── go.mod
    │   ├── go.sum
    │   └── main.go
    ├── BookingServices
    │   ├── src
    │   │   ├── api
    │   │   │   └── hotel.api.ts
    │   │   ├── config
    │   │   │   ├── db.config.js
    │   │   │   ├── index.ts
    │   │   │   ├── logger.config.ts
    │   │   │   ├── redis.config.ts
    │   │   │   └── sequelize.config.js
    │   │   ├── controller
    │   │   │   ├── booking.controller.ts
    │   │   │   └── ping.controller.ts
    │   │   ├── db
    │   │   │   ├── migrations
    │   │   │   │   ├── 20250523102421-Create-Booking-Table.ts
    │   │   │   │   ├── 20250523121044-Add-Total-Guest.ts
    │   │   │   │   ├── 20250523132641-Added-IdompotencyKey-Table.ts
    │   │   │   │   ├── 20250525104536-Added-Finalized-Column-and-update-realtionship.ts
    │   │   │   │   └── 20250818133552-Added-RoomCategoryId-Checkin-Checkout-column.ts
    │   │   │   └── models
    │   │   │       ├── booking.model.ts
    │   │   │       ├── idompotencykey.model.ts
    │   │   │       ├── index.js
    │   │   │       └── sequelize.ts
    │   │   ├── dto
    │   │   │   └── booking.dto.ts
    │   │   ├── middleware
    │   │   │   ├── correlation.middleware.ts
    │   │   │   └── error.middleware.ts
    │   │   ├── repositories
    │   │   │   └── booking.repository.ts
    │   │   ├── router
    │   │   │   └── v1
    │   │   │       ├── booking.router.ts
    │   │   │       ├── index.router.ts
    │   │   │       └── ping.router.ts
    │   │   ├── service
    │   │   │   └── booking.service.ts
    │   │   ├── utils
    │   │   │   ├── Error
    │   │   │   │   └── app.error.ts
    │   │   │   └── Helper
    │   │   │       ├── generateIdompotencyKey.ts
    │   │   │       └── req.helper.ts
    │   │   ├── validators
    │   │   │   ├── booking.validator.ts
    │   │   │   ├── index.ts
    │   │   │   └── ping.validator.ts
    │   │   └── server.ts
    │   ├── .gitignore
    │   └── .sequelizerc
    ├── HotelServices
    │   ├── src
    │   │   ├── config
    │   │   │   ├── db.config.js
    │   │   │   ├── index.ts
    │   │   │   ├── logger.config.ts
    │   │   │   ├── redis.config.ts
    │   │   │   └── sequelize.config.js
    │   │   ├── controller
    │   │   │   ├── hotel.controller.ts
    │   │   │   ├── ping.controller.ts
    │   │   │   ├── roomGeneration.controller.ts
    │   │   │   ├── rooms.controller.ts
    │   │   │   └── roomScheduler.controller.ts
    │   │   ├── db
    │   │   │   ├── migrations
    │   │   │   │   ├── 20250425142746-create-hotel-table.ts
    │   │   │   │   ├── 20250520142556-add-ratings-hotel-table.ts
    │   │   │   │   ├── 20250521094040-add-delete-at-to-hotels.ts
    │   │   │   │   ├── 20250625042101-add-room-table.ts
    │   │   │   │   ├── 20250625055350-add-price-coloum-in-room-table.ts
    │   │   │   │   ├── 20250625095111-add-room-category-table.ts
    │   │   │   │   ├── 20250625110030-add-assocition-to-rooms-table.ts
    │   │   │   │   └── 20250802073333-setting-timestamp-default-value-in-room-category-and-rooms-table.ts
    │   │   │   └── models
    │   │   │       ├── hotel.model.ts
    │   │   │       ├── index.js
    │   │   │       ├── roomcategory.model.ts
    │   │   │       ├── rooms.model.ts
    │   │   │       └── sequelize.ts
    │   │   ├── dto
    │   │   │   ├── hotel.dto.ts
    │   │   │   ├── roomcategory.dto.ts
    │   │   │   ├── roomGeneration.dto.ts
    │   │   │   └── rooms.dto.ts
    │   │   ├── middleware
    │   │   │   ├── correlation.middleware.ts
    │   │   │   └── error.middleware.ts
    │   │   ├── processors
    │   │   │   └── roomGeneration.processor.ts
    │   │   ├── producers
    │   │   │   ├── cron.ts
    │   │   │   └── roomGeneration.producer.ts
    │   │   ├── queue
    │   │   │   └── roomGeneration.queue.ts
    │   │   ├── repositories
    │   │   │   ├── base.repository.ts
    │   │   │   ├── hotel.repository.ts
    │   │   │   ├── room.repository.ts
    │   │   │   └── roomcategory.repository.ts
    │   │   ├── router
    │   │   │   └── v1
    │   │   │       ├── hotel.router.ts
    │   │   │       ├── index.router.ts
    │   │   │       ├── ping.router.ts
    │   │   │       ├── room.router.ts
    │   │   │       ├── roomGeneration.router.ts
    │   │   │       └── roomSchedular.ts
    │   │   ├── scheduler
    │   │   │   └── roomSchedular.ts
    │   │   ├── services
    │   │   │   ├── hotel.services.ts
    │   │   │   ├── room.services.ts
    │   │   │   ├── roomcategory.service.ts
    │   │   │   └── roomGeneration.service.ts
    │   │   ├── utils
    │   │   │   ├── Error
    │   │   │   │   └── app.error.ts
    │   │   │   └── helper
    │   │   │       └── req.helper.ts
    │   │   ├── validators
    │   │   │   ├── hotel.validator.ts
    │   │   │   ├── index.ts
    │   │   │   ├── ping.validators.ts
    │   │   │   └── room.validator.ts
    │   │   └── server.ts
    │   ├── .gitignore
    │   └── .sequelizerc
    ├── NotificationServices
    │   ├── src
    │   │   ├── config
    │   │   │   ├── index.ts
    │   │   │   ├── logger.config.ts
    │   │   │   ├── mailer.config.ts
    │   │   │   └── redis.config.ts
    │   │   ├── controllers
    │   │   │   └── ping.controller.ts
    │   │   ├── dtos
    │   │   │   └── notification.dto.ts
    │   │   ├── middlewares
    │   │   │   ├── correlation.middleware.ts
    │   │   │   └── error.middleware.ts
    │   │   ├── processors
    │   │   │   └── email.processor.ts
    │   │   ├── producers
    │   │   │   └── email.producer.ts
    │   │   ├── queue
    │   │   │   └── email.queue.ts
    │   │   ├── routers
    │   │   │   ├── v1
    │   │   │   │   ├── index.router.ts
    │   │   │   │   └── ping.router.ts
    │   │   │   └── v2
    │   │   │       └── index.router.ts
    │   │   ├── services
    │   │   │   └── mailer.service.ts
    │   │   ├── templates
    │   │   │   ├── mailer
    │   │   │   │   └── welcome.hbs
    │   │   │   └── template.handler.ts
    │   │   ├── utils
    │   │   │   ├── errors
    │   │   │   │   └── app.error.ts
    │   │   │   └── helpers
    │   │   │       └── request.helpers.ts
    │   │   ├── validators
    │   │   │   ├── index.ts
    │   │   │   └── ping.validator.ts
    │   │   └── server.ts
    │   ├── .gitignore
    │   └── README.md
    ├── ReviewService
    │   ├── app
    │   │   └── Application.go
    │   ├── config
    │   │   ├── db
    │   │   │   └── db.go
    │   │   └── env
    │   │       └── env.go
    │   ├── controllers
    │   │   ├── pingHandler.go
    │   │   └── reviewHandler.go
    │   ├── db
    │   │   ├── migrations
    │   │   │   └── 20250727084038_create_review_table.sql
    │   │   └── repositories
    │   │       ├── review.go
    │   │       └── storage.go
    │   ├── dtos
    │   │   └── createReviewDTO.go
    │   ├── models
    │   │   └── Review.go
    │   ├── routers
    │   │   ├── reviewRouter.go
    │   │   └── router.go
    │   ├── schedular
    │   │   └── review_schedular.go
    │   ├── services
    │   │   └── review.go
    │   ├── utils
    │   │   └── json.go
    │   ├── go.mod
    │   ├── go.sum
    │   └── main.go
    └── .gitignore


================================================
FILE: AuthInGoService/app/application.go
================================================
package app

import (
	config "AuthInGo/config/env"
	dbconfig "AuthInGo/config/db"
	"AuthInGo/controllers"
	db "AuthInGo/db/repositories"
	"AuthInGo/routers"
	"AuthInGo/services"
	"fmt"
	"net/http"
	"time"
)

//Config hold the configuration of the Server
type Config struct {
	Addr string //PORT
}

type Application struct {
	Config Config
	Store db.Storage
}

//Constructor
func NewConfig() Config {
	port := config.GetString("PORT" , ":8080")

	return Config{
		Addr: port,
	}
}

func NewApplication(cfg Config) Application {
	return Application{
		Config: cfg,
		Store: *db.NewStorage(),
	}
}

func (app *Application) Run() error {
	repo := dbconfig.DB

	ur := db.NewUserRepository(repo)
	rr := db.NewRoleRepository(repo)
	pr := db.NewPermissionRepository(repo)
	rpr := db.NewRolePermissionRepository(repo)
	urr := db.NewUserRoleRepository(repo)
	us := services.NewUserService(ur)
	rs := services.NewRoleService(rr , rpr , urr)
	ps := services.NewPermissionService(pr)
	uc := controllers.NewUserController(us)
	rc := controllers.NewRoleController(rs)
	pc := controllers.NewPermissionController(ps)
	uRouter := routers.NewUserRouter(uc)
	rRouter := routers.NewRoleRouter(rc)
	pRouter := routers.NewPermissionRouter(pc)


	server := &http.Server{
		Addr: app.Config.Addr,
		Handler: routers.SetupRouter(uRouter , rRouter , pRouter),
		ReadTimeout: 10 * time.Second,
		WriteTimeout: 10 * time.Second,
	}
	fmt.Println("Server is running on port :" , app.Config.Addr) ; 

	return server.ListenAndServe() ; 
}




================================================
FILE: AuthInGoService/config/db/db.go
================================================
package config

import (
	config "AuthInGo/config/env"
	"database/sql"
	"fmt"

	"github.com/go-sql-driver/mysql"
)

var DB *sql.DB

func InitDB(){
	var err error
	DB , err = setupDB()

	if err != nil {
		fmt.Println("Error setting up DB connection" , err)
		return
	}
}

func setupDB() (*sql.DB , error){
	cfg := mysql.NewConfig()

	cfg.User = config.GetString("DB_USER" , "root")
	cfg.Passwd = config.GetString("DB_PASSWORD" , "root")
	cfg.Net = config.GetString("DB_TCP" , "tcp")
	cfg.Addr = config.GetString("DB_ADDR" , "127.0.0.1:3306")
	cfg.DBName = config.GetString("DB_NAME" , "AuthDB")

	fmt.Println("Connecting to database:", cfg.DBName, cfg.FormatDSN())
	//from this config it convert to DSN string
	db, err := sql.Open("mysql", cfg.FormatDSN())

	if err != nil {
		fmt.Println("Error connecting to database:", err)
		return nil, err
	}

	fmt.Println(("Trying to connect to database..."))
	//verify database connection
	pingErr := db.Ping()
	if pingErr != nil {
		fmt.Println("Error pinging database:", pingErr)
		return nil, pingErr
	}
	fmt.Println("Connected to database successfully:", cfg.DBName)

	return db, nil
}

================================================
FILE: AuthInGoService/config/env/env.go
================================================
package config

import (
	"fmt"
	"os"
	"strconv"

	"github.com/joho/godotenv"
)

func Load() {
	err := godotenv.Load()

	if err != nil {
		// Log the error if the .env file is not found or cannot be 
		// loaded
		fmt.Println("Error loading .env file")
	}
}

func GetString(key string, fallback string) string {
	value, ok := os.LookupEnv(key)

	if !ok {
		return fallback
	}

	return value

}

func GetInt(key string, fallback int) int {
	value, ok := os.LookupEnv(key)

	if !ok {
		return fallback
	}

	intValue, err := strconv.Atoi(value)

	if err != nil {
		fmt.Printf("Error converting %s to int: %v\n", key, err)
		return fallback
	}

	return intValue
}

func GetBool(key string, fallback bool) bool {
	value, ok := os.LookupEnv(key)

	if !ok {
		return fallback
	}

	boolValue, err := strconv.ParseBool(value)

	if err != nil {
		fmt.Printf("Error converting %s to bool: %v\n", key, err)
		return fallback
	}

	return boolValue
}

================================================
FILE: AuthInGoService/controllers/permission.go
================================================
package controllers

import (
	"AuthInGo/dtos"
	"AuthInGo/services"
	"AuthInGo/utils"
	"net/http"
	"strconv"

	"github.com/go-chi/chi/v5"
)

type PermissionController struct {
	permissionService services.PermissionService
}

func NewPermissionController(_roleService services.PermissionService) *PermissionController {
	return &PermissionController{
		permissionService: _roleService,
	}
}

func (pc *PermissionController) GetPermissionById(w http.ResponseWriter , r *http.Request) {
	id := chi.URLParam(r , "id")

	intId , _ := strconv.Atoi(id)

	permission , err := pc.permissionService.GetPermissionById(int64(intId))

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in fetching permission by id" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Fetched permission successfully" , http.StatusOK , permission)
}

func (pc *PermissionController) GetPermissionByName(w http.ResponseWriter , r *http.Request) {
	name := r.URL.Query().Get("name")

	if name == "" {
		roles , err := pc.permissionService.GetAllPermissions()

		if err != nil {
			utils.WriteErrorJsonResponse(w , "Error in fetching all roles" , http.StatusInternalServerError , err)
			return
		}
		utils.WriteSuccessJsonResponse(w , "Fetched roles successfully" , http.StatusOK , roles)
		return 
	}

	permission , err := pc.permissionService.GetPermissionByName(name)

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in fetching permission by name" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Fetched permission successfully" , http.StatusOK , permission)
}

func (pc *PermissionController) CreatePermission(w http.ResponseWriter  , r *http.Request) {
	var payload *dtos.CreatePermissionRequestDTO

	err := utils.ReadJsonBody(r , &payload)
	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in reading json" , http.StatusInternalServerError , err)
		return
	}

	permission , err := pc.permissionService.CreatePermission(payload)

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in creating permission" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Permission created successfully" , http.StatusOK , permission)
}

func (pc *PermissionController) DeleteById(w http.ResponseWriter , r *http.Request) {
	id := chi.URLParam(r , "id")

	intId , _ := strconv.Atoi(id)

	err := pc.permissionService.DeletePermissionById(int64(intId))

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in deleting permission by id" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Permission deleted successfully" , http.StatusOK , "")
}

func (pc *PermissionController) UpdateById(w http.ResponseWriter , r *http.Request) {
	id := chi.URLParam(r , "id")

	var payload *dtos.CreatePermissionRequestDTO

	err := utils.ReadJsonBody(r , &payload)
	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in reading json" , http.StatusInternalServerError , err)
		return
	}

	intId , _ := strconv.Atoi(id)

	permission , err := pc.permissionService.UpdatePermissionById(int64(intId) , payload)

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in updating permission by id" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Permission updated successfully" , http.StatusOK , permission)
}


================================================
FILE: AuthInGoService/controllers/ping.go
================================================
package controllers

import "net/http"

func PingHandeler(w http.ResponseWriter , r *http.Request){
	w.Write([]byte ("Pong"))
}

================================================
FILE: AuthInGoService/controllers/role.go
================================================
package controllers

import (
	"AuthInGo/dtos"
	"AuthInGo/services"
	"AuthInGo/utils"
	"fmt"
	"net/http"
	"strconv"

	"github.com/go-chi/chi/v5"
)

type RoleController struct {
	roleService services.RoleService
}

func NewRoleController(_roleService services.RoleService) *RoleController {
	return &RoleController{
		roleService: _roleService,
	}
}

func (rc *RoleController) GetRoleById(w http.ResponseWriter , r *http.Request) {
	id := chi.URLParam(r , "id")

	intId , _ := strconv.Atoi(id)

	role , err := rc.roleService.GetRoleById(int64(intId))

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in fetching role by id" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Fetched role successfully" , http.StatusOK , role)
}

func (rc *RoleController) GetRoleByName(w http.ResponseWriter , r *http.Request) {
	name := r.URL.Query().Get("name")

	if name == "" {
		roles , err := rc.roleService.GetAllRoles()

		if err != nil {
			utils.WriteErrorJsonResponse(w , "Error in fetching all roles" , http.StatusInternalServerError , err)
			return
		}
		utils.WriteSuccessJsonResponse(w , "Fetched roles successfully" , http.StatusOK , roles)
		return 
	}

	role , err := rc.roleService.GetRoleByName(name)

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in fetching role by name" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Fetched role successfully" , http.StatusOK , role)
}

func (rc *RoleController) CreateRole(w http.ResponseWriter  , r *http.Request) {
	var payload *dtos.CreateRoleRequestDTO

	err := utils.ReadJsonBody(r , &payload)
	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in reading json" , http.StatusInternalServerError , err)
		return
	}

	role , err := rc.roleService.CreateRole(payload)

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in creating role" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Role created successfully" , http.StatusOK , role)
}

func (rc *RoleController) DeleteById(w http.ResponseWriter , r *http.Request) {
	id := chi.URLParam(r , "id")

	intId , _ := strconv.Atoi(id)

	err := rc.roleService.DeleteRoleById(int64(intId))

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in deleting role by id" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Role deleted successfully" , http.StatusOK , "")
}

func (rc *RoleController) UpdateById(w http.ResponseWriter , r *http.Request) {
	id := chi.URLParam(r , "id")

	var payload *dtos.CreateRoleRequestDTO

	err := utils.ReadJsonBody(r , &payload)
	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in reading json" , http.StatusInternalServerError , err)
		return
	}

	intId , _ := strconv.Atoi(id)

	role , err := rc.roleService.UpdateRoleById(int64(intId) , payload)

	if err != nil {
		utils.WriteErrorJsonResponse(w , "Error in updating role by id" , http.StatusInternalServerError , err)
		return
	}
	utils.WriteSuccessJsonResponse(w , "Role updated successfully" , http.StatusOK , role)
}

func (rc *RoleController) AssignRoleToUser(w http.ResponseWriter, r *http.Request) {
	userId := chi.URLParam(r, "userId")
	roleId := chi.URLParam(r, "roleId")
	if userId == "" {
		utils.WriteErrorJsonResponse(w,  "User ID is required", http.StatusBadRequest, fmt.Errorf("missing user ID"))
		return
	}
	if roleId == "" {
		utils.WriteErrorJsonResponse(w, "Role ID is required", http.StatusBadRequest, fmt.Errorf("missing role ID"))
		return
	}

	roleIdInt, err := strconv.ParseInt(roleId, 10, 64)
	if err != nil {
		utils.WriteErrorJsonResponse(w,  "Invalid role ID", http.StatusBadRequest, err)
		return
	}

	userIdInt, err := strconv.ParseInt(userId, 10, 64)
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Invalid user ID", http.StatusBadRequest, err)
		return
	}

	err = rc.roleService.AssignRoleToUser(userIdInt, roleIdInt)
	if err != nil {
		utils.WriteErrorJsonResponse(w , "Failed to assign role to user", http.StatusInternalServerError, err)
		return
	}

	utils.WriteSuccessJsonResponse(w, "Role assigned to user successfully", http.StatusOK, nil)
}

func (rc *RoleController) GetRolePermissions(w http.ResponseWriter, r *http.Request) {
	roleId := chi.URLParam(r, "id")
	if roleId == "" {
		utils.WriteErrorJsonResponse(w, "Role ID is required",  http.StatusBadRequest , fmt.Errorf("missing role ID"))
		return
	}

	id, err := strconv.ParseInt(roleId, 10, 64)
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Invalid role ID" , http.StatusBadRequest, err)
		return
	}

	rolePermissions, err := rc.roleService.GetRolePermissions(id)
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Failed to fetch role permissions", http.StatusInternalServerError, err)
		return
	}

	utils.WriteSuccessJsonResponse(w, "Role permissions fetched successfully", http.StatusOK, rolePermissions)
}

func (rc *RoleController) AssignPermissionToRole(w http.ResponseWriter, r *http.Request) {
	roleId := chi.URLParam(r, "id")
	if roleId == "" {
		utils.WriteErrorJsonResponse(w, "Role ID is required", http.StatusBadRequest, fmt.Errorf("missing role ID"))
		return
	}

	id, err := strconv.ParseInt(roleId, 10, 64)
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Invalid role ID", http.StatusBadRequest, err)
		return
	}

	payload := r.Context().Value("payload").(dtos.AssignPermissionRequestDTO)

	rolePermission, err := rc.roleService.AddPermissionToRole(id, payload.PermissionId)
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Failed to assign permission to role", http.StatusInternalServerError, err)
		return
	}

	utils.WriteSuccessJsonResponse(w, "Permission assigned to role successfully", http.StatusCreated, rolePermission)
}

func (rc *RoleController) RemovePermissionFromRole(w http.ResponseWriter, r *http.Request) {
	roleId := chi.URLParam(r, "id")
	if roleId == "" {
		utils.WriteErrorJsonResponse(w, "Role ID is required", http.StatusBadRequest, fmt.Errorf("missing role ID"))
		return
	}

	id, err := strconv.ParseInt(roleId, 10, 64)
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Invalid role ID", http.StatusBadRequest, err)
		return
	}

	payload := r.Context().Value("payload").(dtos.RemovePermissionRequestDTO)

	err = rc.roleService.RemovePermissionFromRole(id, payload.PermissionId)
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Failed to remove permission from role", http.StatusInternalServerError, err)
		return
	}

	utils.WriteSuccessJsonResponse(w, "Permission removed from role successfully", http.StatusOK, nil)
}

func (rc *RoleController) GetAllRolePermissions(w http.ResponseWriter, r *http.Request) {
	rolePermissions, err := rc.roleService.GetAllRolePermissions()
	if err != nil {
		utils.WriteErrorJsonResponse(w, "Failed to fetch all role permissions", http.StatusInternalServerError, err)
		return
	}

	utils.WriteSuccessJsonResponse(w, "All role permissions fetched successfully", http.StatusOK, rolePermissions)
}

================================================
FILE: AuthInGoService/controllers/user.go
================================================
package controllers

import (
	"AuthInGo/dtos"
	"AuthInGo/services"
	"AuthInGo/utils"
	"fmt"
	"net/http"
)

type UserController struct {
	userService services.UserService
}

func NewUserController(_userService services.UserService) *UserController{
	return &UserController{
		userService: _userService,
	}
}

func (uc *UserController) GetUserById(w http.ResponseWriter , r *http.Request){
	fmt.Println("Register User called in User Controller.")
	userId := r.URL.Query().Get("id")
	if userId == "" {
		userId = r.Context().Value("userId").(string) 
	}

	fmt.Println("User ID from context or query:", userId)


	user , err := uc.userService.GetUserById(userId)

	if err != nil {
		fmt.Println("Error in fetching the user" , err)
		utils.WriteErrorJsonResponse(w , "User Fetching Error" , http.StatusInternalServerError , err)
		return
	}
	
	utils.WriteSuccessJsonResponse(w , "User Found" , http.StatusFound , user)
}

func (uc *UserController) Create(w http.ResponseWriter , r *http.Request) {
	fmt.Println("Register User called in User Controller.")

	payload := r.Context().Value("validatedPayload").(dtos.CreateUserRequest)
	
	uc.userService.CreateUser(&payload)
	utils.WriteSuccessJsonResponse(w , "User Sigup Successfull" , http.StatusAccepted , "")
}

func (uc *UserController) LoginUser(w http.ResponseWriter , r *http.Request){
	fmt.Println("Login User called in User Controller.")
	 
	payload := r.Context().Value("validatedPayload").(dtos.LoginUserRequest)

	jwtToken , err := uc.userService.LoginUser(&payload)
	
	if err != nil {
		utils.WriteErrorJsonResponse(w , "Wrong Credentials" , http.StatusNotAcceptable , err)
		return
	}

	utils.WriteSuccessJsonResponse(w , "User Login Successfull" , http.StatusAccepted , jwtToken)
}

================================================
FILE: AuthInGoService/db/migrations/20250721124056_create_users_table.sql
================================================
-- +goose Up
-- +goose StatementBegin
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
-- +goose StatementEnd

-- +goose Down
-- +goose StatementBegin
DROP TABLE USERS;
-- +goose StatementEnd


================================================
FILE: AuthInGoService/db/migrations/20250729095851_create_role_table.sql
================================================
-- +goose Up
-- +goose StatementBegin
CREATE TABLE IF NOT EXISTS ROLE(
    ID SERIAL PRIMARY KEY , 
    NAME VARCHAR(50) NOT NULL UNIQUE, 
    DESCRIPTION TEXT , 
    CREATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP , 
    UPDATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
)
-- +goose StatementEnd

-- +goose Down
-- +goose StatementBegin
DROP TABLE IF EXISTS ROLE;
-- +goose StatementEnd


================================================
FILE: AuthInGoService/db/migrations/20250729100519_create_permission_table.sql
================================================
-- +goose Up
-- +goose StatementBegin
CREATE TABLE IF NOT EXISTS PERMISSION(
    ID SERIAL PRIMARY KEY  , 
    NAME VARCHAR(50) NOT NULL UNIQUE, 
    DESCRIPTION TEXT , 
    RESOURCE VARCHAR(50) NOT NULL , 
    ACTION VARCHAR(50) NOT NULL , 
    CREATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP , 
    UPDATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
)
-- +goose StatementEnd

-- +goose Down
-- +goose StatementBegin
DROP TABLE IF EXISTS PERMISSION ; 
-- +goose StatementEnd


================================================
FILE: AuthInGoService/db/migrations/20250729101222_role_permission_table.sql
================================================
-- +goose Up
-- +goose StatementBegin
CREATE TABLE IF NOT EXISTS ROLE_PERMISSION(
    ID SERIAL PRIMARY KEY , 
    ROLE_ID BIGINT UNSIGNED NOT NULL , 
    PERMISSION_ID BIGINT UNSIGNED NOT NULL , 
    CREATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP , 
    UPDATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP , 

    CONSTRAINT FK_ROLE_PERMISSION_ROLE FOREIGN KEY (ROLE_ID) REFERENCES ROLE(ID) ON DELETE CASCADE,
    CONSTRAINT FK_ROLE_PERMISSION_PERMISSION FOREIGN KEY (PERMISSION_ID) REFERENCES PERMISSION(ID) ON DELETE CASCADE
) ; 
-- +goose StatementEnd

-- +goose Down
-- +goose StatementBegin
DROP TABLE IF EXISTS ROLE_PERMISSION;
-- +goose StatementEnd


================================================
FILE: AuthInGoService/db/migrations/20250729102812_create_user_role.sql
================================================
-- +goose Up
-- +goose StatementBegin
CREATE TABLE IF NOT EXISTS USER_ROLE(
    ID SERIAL PRIMARY KEY , 
    USER_ID INT NOT NULL , 
    ROLE_ID BIGINT UNSIGNED NOT NULL , 
    CREATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP , 
    UPDATED_AT TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP , 

    CONSTRAINT FK_USER_ROLE_USER FOREIGN KEY (USER_ID) REFERENCES USERS(ID) ON DELETE CASCADE , 
    CONSTRAINT FK_USER_ROLE_ROLE FOREIGN KEY (ROLE_ID) REFERENCES ROLE(ID) ON DELETE CASCADE
)
-- +goose StatementEnd

-- +goose Down
-- +goose StatementBegin
DROP TABLE IF EXISTS USER_ROLE ; 
-- +goose StatementEnd


================================================
FILE: AuthInGoService/db/repositories/permission.go
================================================
package db

import (
	"AuthInGo/dtos"
	"AuthInGo/models"
	"database/sql"
)

type PermissionRepository interface {
	GetPermissionById(id int64) (*models.Permission, error)
	GetPermissionByName(name string) (*models.Permission, error)
	GetAllPermissions() ([]*models.Permission, error)
	CreatePermission(payload *dtos.CreatePermissionRequestDTO) (*models.Permission, error)
	DeletePermissionById(id int64) error
	UpdatePermission(id int64, payload *dtos.CreatePermissionRequestDTO) (*models.Permission, error)
}

type PermissionRepositoryImpl struct {
	db *sql.DB
}

func NewPermissionRepository(_db *sql.DB) PermissionRepository {
	return &PermissionRepositoryImpl{
		db: _db,
	}
}

func (p *PermissionRepositoryImpl) GetPermissionById(id int64) (*models.Permission, error) {
	query := "SELECT * FROM permission WHERE ID = ?"
	row := p.db.QueryRow(query, id)

	permission := &models.Permission{}
	if err := row.Scan(&permission.Id, &permission.Name, &permission.Description, &permission.Resource, &permission.Action, &permission.CreatedAt, &permission.UpdatedAt); err != nil {
		return nil, err
	}
	return permission, nil
}

func (p *PermissionRepositoryImpl) GetPermissionByName(name string) (*models.Permission, error) {
	query := "SELECT * FROM permission WHERE NAME = ?"
	row := p.db.QueryRow(query, name)

	permission := &models.Permission{}
	if err := row.Scan(&permission.Id, &permission.Name, &permission.Description, &permission.Resource, &permission.Action, &permission.CreatedAt, &permission.UpdatedAt); err != nil {
		return nil, err
	}
	return permission, nil
}

func (p *PermissionRepositoryImpl) GetAllPermissions() ([]*models.Permission, error) {
	query := "SELECT * FROM permission"
	rows, err := p.db.Query(query)
	if err != nil {
		return nil, err
	}
	defer rows.Close()

	var permissions []*models.Permission
	for rows.Next() {
		permission := &models.Permission{}
		if err := rows.Scan(&permission.Id, &permission.Name, &permission.Description, &permission.Resource, &permission.Action, &permission.CreatedAt, &permission.UpdatedAt); err != nil {
			return nil, err
		}
		permissions = append(permissions, permission)
	}

	if err := rows.Err(); err != nil {
		return nil, err
	}

	return permissions, nil
}

func (p *PermissionRepositoryImpl) CreatePermission(payload *dtos.CreatePermissionRequestDTO) (*models.Permission, error) {
	query := "INSERT INTO permission (name, description, resource, action, created_at, updated_at) VALUES (?, ?, ?, ?, NOW(), NOW())"
	result, err := p.db.Exec(query, payload.Name, payload.Description, payload.Resource, payload.Action)
	if err != nil {
		return nil, err
	}

	id, err := result.LastInsertId()
	if err != nil {
		return nil, err
	}

	return &models.Permission{
		Id:          id,
		Name:        payload.Name,
		Description: payload.Description,
		Resource:    payload.Resource,
		Action:      payload.Action,
		CreatedAt:   "NOW()",
		UpdatedAt:   "NOW()",
	}, nil
}

func (p *PermissionRepositoryImpl) DeletePermissionById(id int64) error {
	query := "DELETE FROM permission WHERE id = ?"
	result, err := p.db.Exec(query, id)
	if err != nil {
		return err
	}
	rowsAffected, err := result.RowsAffected()
	if err != nil {
		return err
	}
	if rowsAffected == 0 {
		return sql.ErrNoRows
	}
	return nil
}
func (p *PermissionRepositoryImpl) UpdatePermission(id int64, payload *dtos.CreatePermissionRequestDTO) (*models.Permission, error) {
	query := "UPDATE permission SET name = ?, description = ?, resource = ?, action = ?, updated_at = NOW() WHERE id = ?"
	_, err := p.db.Exec(query, payload.Name, payload.Description, payload.Resource, payload.Action, id)
	if err != nil {
		return nil, err
	}

	return &models.Permission{
		Id:          id,
		Name:        payload.Name,
		Description: payload.Description,
		Resource:    payload.Resource,
		Action:      payload.Action,
		CreatedAt:   "NOW()",
		UpdatedAt:   "NOW()",
	}, nil
}

================================================
FILE: AuthInGoService/db/repositories/role.go
================================================
package db

import (
	"AuthInGo/dtos"
	"AuthInGo/models"
	"database/sql"
	"fmt"
	"time"
)

type RoleRepository interface {
	GetById(id int64) (*models.Role , error)
	GetByName(name string) (*models.Role , error)
	GetAll() ([]*models.Role , error)
	Create(payload *dtos.CreateRoleRequestDTO) (*models.Role , error)
	DeleteById(id int64) error 
	UpdateById(id int64 , payload *dtos.CreateRoleRequestDTO) (*models.Role , error)
}

type RoleRepositoryImpl struct {
	db *sql.DB
}

func NewRoleRepository(_db *sql.DB) RoleRepository {
	return &RoleRepositoryImpl{
		db : _db , 
	}
}


func (r *RoleRepositoryImpl) GetById(id int64) (*models.Role , error) {
	query := "SELECT * FROM ROLE WHERE ID = ?"

	row := r.db.QueryRow(query , id)

	role := &models.Role{}
	err := row.Scan(&role.Id , &role.Name , &role.Description , &role.Created_at , &role.Updated_at)

	if err != nil { 
		if err == sql.ErrNoRows {
			fmt.Println("No record Found!")
		} else {
			fmt.Println("Error scanning row")
		}
		return nil , err
	}

	fmt.Println("Role Fetched Successfully")
	return role , nil
}

func (r *RoleRepositoryImpl) GetByName(name string) (*models.Role , error) {
	query := "SELECT * FROM ROLE WHERE NAME = ?;"

	row := r.db.QueryRow(query , name)
	role := &models.Role{}

	err := row.Scan(&role.Id , &role.Name , &role.Description , &role.Created_at , &role.Updated_at)
	
	if err != nil {
		if err == sql.ErrNoRows {
			fmt.Println("No records found!")
		} else { 
			fmt.Println("Error scanning the row")
		}
		return nil , err
	}
	return role , nil
}

func (r *RoleRepositoryImpl) GetAll() ([]*models.Role , error) {
	query := "SELECT * FROM ROLE;"

	rows , err := r.db.Query(query)

	if err != nil {
		if err == sql.ErrNoRows {
			fmt.Println("No records found!")
		} else { 
			fmt.Println("Error scanning the row")
		}
		return nil , err
	}

	var roles []*models.Role
	for rows.Next() {
		role := &models.Role{}
		err := rows.Scan(&role.Id , &role.Name , &role.Description , &role.Created_at , &role.Updated_at)
		
		if err != nil {
			fmt.Println("Error in scannning role.")
			return nil , err
		}
		roles = append(roles, role)
	}
	return roles , nil
}

func (r *RoleRepositoryImpl) Create(payload *dtos.CreateRoleRequestDTO) (*models.Role , error) {
	query := "INSERT INTO ROLE ( NAME , DESCRIPTION ) VALUES ( ? , ?) ;"

	result , err := r.db.Exec(query , payload.Name , payload.Description)

	if err != nil {
		fmt.Println("Error in creating the role!" , err)
		return nil , err
	}

	lastEnterId , lastInsertIdErr := result.LastInsertId()

	if lastInsertIdErr != nil {
		fmt.Println("Error in getting last enteredId" , lastInsertIdErr)
		return nil , lastInsertIdErr
	}

	role := &models.Role{
		Id: lastEnterId,
		Name: payload.Name,
		Description: payload.Description,
		Created_at: time.Now().String(),
		Updated_at: time.Now().String(),
	}

	fmt.Println("Role created successfully!")
	return role , nil 
}

func (r *RoleRepositoryImpl) DeleteById(id int64) error {
	query := "DELETE FROM ROLE WHERE ID = ?;"

	result , err := r.db.Exec(query , id)

	if err != nil { 
		if err == sql.ErrNoRows {
			fmt.Println("No row found to delete")
		} else  {
			fmt.Println("Error in executing the query")
		}
		return err
	}

	rowsAffected , rowsAffectedErr := result.RowsAffected()
	if rowsAffectedErr != nil {
		fmt.Println("Error getting rows affected:", rowsAffectedErr)
		return rowsAffectedErr
	}
	if rowsAffected == 0 {
		fmt.Println("No rows were affected, user not deleted")
		return rowsAffectedErr
	}

	fmt.Println("Row deleted succesfully!")
	return nil 
}

func (r *RoleRepositoryImpl) UpdateById(id int64 , payload *dtos.CreateRoleRequestDTO) (*models.Role , error){
	query := "UPDATE role SET name = COALESCE(?, name), description = COALESCE(?, description) WHERE id = ?"
	result , err := r.db.Exec(query, payload.Name , payload.Description , id)

	if err != nil { 
		if err == sql.ErrNoRows {
			fmt.Println("No row found to update")
		} else  {
			fmt.Println("Error in executing the query")
		}
		return nil , err
	}
	rowsAffected , rowsAffectedErr := result.RowsAffected()
	if rowsAffectedErr != nil {
		fmt.Println("Error getting rows affected:", rowsAffectedErr)
		return nil , rowsAffectedErr
	}
	if rowsAffected == 0 {
		fmt.Println("No rows were affected, role not updated")
		return nil , rowsAffectedErr
	}

	fmt.Println("Row updated succesfully!")

	role := &models.Role{
		Id: id,
		Name: payload.Name,
		Description: payload.Description,
		Created_at: "",
		Updated_at: time.Now().String(),
	}
	return role , nil 
}

================================================
FILE: AuthInGoService/db/repositories/role_permission.go
================================================
package db

import (
	"AuthInGo/models"
	"database/sql"
)

type RolePermissionRepository interface {
	GetRolePermissionById(id int64) (*models.RolePermission, error)
	GetRolePermissionByRoleId(roleId int64) ([]*models.RolePermission, error)
	AddPermissionToRole(roleId int64, permissionId int64) (*models.RolePermission, error)
	RemovePermissionFromRole(roleId int64, permissionId int64) error
	GetAllRolePermissions() ([]*models.RolePermission, error)
}

type RolePermissionRepositoryImpl struct {
	db *sql.DB
}

func NewRolePermissionRepository(_db *sql.DB) RolePermissionRepository {
	return &RolePermissionRepositoryImpl{
		db: _db,
	}
}

func (rp *RolePermissionRepositoryImpl) GetRolePermissionById(id int64) (*models.RolePermission, error) {
	query := "SELECT id, role_id, permission_id, created_at, updated_at FROM role_permission WHERE id = ?"
	row := rp.db.QueryRow(query, id)

	rolePermission := &models.RolePermission{}
	if err := row.Scan(&rolePermission.Id, &rolePermission.RoleId, &rolePermission.PermissionId, &rolePermission.CreatedAt, &rolePermission.UpdatedAt); err != nil {
		return nil, err
	}
	return rolePermission, nil
}

func (rp *RolePermissionRepositoryImpl) GetRolePermissionByRoleId(roleId int64) ([]*models.RolePermission, error) {
	query := "SELECT id, role_id, permission_id, created_at, updated_at FROM role_permission WHERE role_id = ?"
	rows, err := rp.db.Query(query, roleId)
	if err != nil {
		return nil, err
	}
	defer rows.Close()

	var rolePermissions []*models.RolePermission
	for rows.Next() {
		rolePermission := &models.RolePermission{}
		if err := rows.Scan(&rolePermission.Id, &rolePermission.RoleId, &rolePermission.PermissionId, &rolePermission.CreatedAt, &rolePermission.UpdatedAt); err != nil {
			return nil, err
		}
		rolePermissions = append(rolePermissions, rolePermission)
	}

	if err := rows.Err(); err != nil {
		return nil, err
	}

	return rolePermissions, nil
}

func (rp *RolePermissionRepositoryImpl) AddPermissionToRole(roleId int64, permissionId int64) (*models.RolePermission, error) {
	query := "INSERT INTO role_permission (role_id, permission_id, created_at, updated_at) VALUES (?, ?, NOW(), NOW())"
	result, err := rp.db.Exec(query, roleId, permissionId)
	if err != nil {
		return nil, err
	}

	id, err := result.LastInsertId()
	if err != nil {
		return nil, err
	}

	return &models.RolePermission{
		Id:           id,
		RoleId:       roleId,
		PermissionId: permissionId,
		CreatedAt:    "NOW()",
		UpdatedAt:    "NOW()",
	}, nil
}

func (rp *RolePermissionRepositoryImpl) RemovePermissionFromRole(roleId int64, permissionId int64) error {
	query := "DELETE FROM role_permission WHERE role_id = ? AND permission_id = ?"
	result, err := rp.db.Exec(query, roleId, permissionId)
	if err != nil {
		return err
	}

	rowsAffected, err := result.RowsAffected()
	if err != nil {
		return err
	}

	if rowsAffected == 0 {
		return sql.ErrNoRows
	}

	return nil
}

func (rp *RolePermissionRepositoryImpl) GetAllRolePermissions() ([]*models.RolePermission, error) {
	query := "SELECT id, role_id, permission_id, created_at, updated_at FROM role_permission"
	rows, err := rp.db.Query(query)
	if err != nil {
		return nil, err
	}
	defer rows.Close()

	var rolePermissions []*models.RolePermission
	for rows.Next() {
		rolePermission := &models.RolePermission{}
		if err := rows.Scan(&rolePermission.Id, &rolePermission.RoleId, &rolePermission.PermissionId, &rolePermission.CreatedAt, &rolePermission.UpdatedAt); err != nil {
			return nil, err
		}
		rolePermissions = append(rolePermissions, rolePermission)
	}

	if err := rows.Err(); err != nil {
		return nil, err
	}

	return rolePermissions, nil
}

================================================
FILE: AuthInGoService/db/repositories/storage.go
================================================
package db

type Storage struct {
	UserRepository UserRepository
}

func NewStorage() *Storage {
	return &Storage{
		UserRepository: &UserRepositoryImpl{},
	}
}

================================================
FILE: AuthInGoService/db/repositories/user.go
================================================
package db

import (
	"AuthInGo/models"
	"database/sql"
	"fmt"
)

type UserRepository interface {
	GetById(id string) (*models.User , error)
	GetAll() ([]*models.User , error)
	Create(username string , email string , hashedPassword string) (*models.User , error)
	GetByEmail(email string) (*models.User , error)
	DeleteById(id string) error
}

type UserRepositoryImpl struct {
	db *sql.DB
}

func NewUserRepository(_db *sql.DB) UserRepository {
	return &UserRepositoryImpl{
		db: _db,
	}
}

func (u *UserRepositoryImpl) DeleteById(id string) error {
	query := "DELETE FROM users WHERE id = ?"
	result, err := u.db.Exec(query, id)

	if err != nil {
		fmt.Println("Error deleting user:", err)
		return err
	}

	rowsAffected, rowErr := result.RowsAffected()
	if rowErr != nil {
		fmt.Println("Error getting rows affected:", rowErr)
		return rowErr
	}
	if rowsAffected == 0 {
		fmt.Println("No rows were affected, user not deleted")
		return nil
	}
	fmt.Println("User deleted successfully, rows affected:", rowsAffected)
	return nil
}

func (u *UserRepositoryImpl) GetByEmail(email string) (*models.User , error){
	query := "SELECT * FROM USERS WHERE EMAIL = ?"

	row := u.db.QueryRow(query , email)
	
	user := &models.User{}
	err := row.Scan(&user.Id , &user.Username , &user.Email , &user.Password , &user.CreatedAt , &user.UpdatedAt)

	if err != nil {
		if err == sql.ErrNoRows {
			fmt.Println("No Records Found!")
			return nil , err
		} else {
			fmt.Println("Error scanning user:", err)
			return nil, err
		}
	}

	return user , nil
}

func (u *UserRepositoryImpl) Create(username string , email string , hashedPassword string) (*models.User , error) {
	query := "INSERT INTO USERS (USERNAME , EMAIL , PASSWORD) VALUES ( ? , ? , ?)"

	result , err := u.db.Exec(query , username , email , hashedPassword)
	if err != nil {
		fmt.Println("Error creating the user")
		return nil , err
	}

	lastEnterId , err := result.LastInsertId()
	if err != nil {
		fmt.Println("Error in getting last entered id" , err)
		return nil , err
	}

	user := &models.User{
		Id: lastEnterId,
		Username: username,
		Email: email,
	}

	fmt.Println("User created Succesfully" , user)
	return user , nil
}


func (u *UserRepositoryImpl) GetAll() ([]*models.User , error){
	query := "SELECT * FROM USERS"

	rows ,err := u.db.Query(query)

	if err != nil {
		fmt.Println("Error fetching the rows from DB" , err)
		return nil, err
	}

	defer rows.Close() // Ensure rows are closed after processing

	var users []*models.User
	for rows.Next() {
		user := &models.User{}
		err := rows.Scan(&user.Id , &user.Username , &user.Email , &user.Password , &user.CreatedAt , &user.UpdatedAt)
		if err != nil {
			fmt.Println("Error fetching the user" , err)
			return nil , err
		}
		users = append(users, user)
	}

	if err := rows.Err(); err != nil {
		fmt.Println("Error with rows:", err)
		return nil , err
	}

	return users , nil 
}

func (u *UserRepositoryImpl) GetById(id string)(*models.User , error){
	fmt.Println("Getting in User Repository")

	//sql injections
	query := "SELECT * FROM USERS WHERE ID = ?"
	row := u.db.QueryRow(query , id)

	user := &models.User{}

	err := row.Scan(&user.Id , &user.Username , &user.Email , &user.Password , &user.CreatedAt , &user.UpdatedAt)

	if err != nil {
		if err == sql.ErrNoRows {
			fmt.Println("No Records Found!")
			return nil , err
		} else {
			fmt.Println("Error scanning user:", err)
			return nil, err
		}
	}
	fmt.Println("Uer fetched Successfully :" , user)
	return user, nil
}

================================================
FILE: AuthInGoService/db/repositories/user_role.go
================================================
package db

import (
	"AuthInGo/models"
	"database/sql"
	"fmt"
	"strings"
)

type UserRoleRepository interface {
	GetUserRole(userId int64) ([]*models.Role , error)
	AssignRoleToUser(userId int64 , roleId int64) error
	RemoveRoleFromUser(userId int64, roleId int64) error
	GetUserPermissions(userId int64) ([]*models.Permission, error)
	HasPermission(userId int64, permissionName string) (bool, error)
	HasRole(userId int64, roleName string) (bool, error)
	HasAllRoles(userId int64, roleNames []string) (bool, error)
	HasAnyRole(userId int64, roleNames []string) (bool, error)
}

type UserRoleRepositoryImpl struct {
	db *sql.DB
}

func NewUserRoleRepository(_db *sql.DB) UserRoleRepository {
	return &UserRoleRepositoryImpl{
		db : _db ,
	}
}

func (u *UserRoleRepositoryImpl) GetUserRole(userId int64) ([]*models.Role , error){
	query := `SELECT R.ID , R.NAME , R.DESCRIPTION , R.CREATED_AT , R.UPDATED_AT 
			  FROM USER_ROLE UR
			  INNER JOIN ROLE R ON R.ID = UR.ID 
			  WHERE USER_ID = ?;`
	
	rows , err := u.db.Query(query , userId)

	if err != nil {
		if err == sql.ErrNoRows {
			fmt.Println("No role found for particular user id" , err)
		} else {
			fmt.Println("Error in quering" , err)
		}
		return nil , err
	}

	defer rows.Close()

	var roles []*models.Role
	
	for rows.Next() {
		role := &models.Role{}
		err := rows.Scan(&role.Id , &role.Name , &role.Description , &role.Created_at , &role.Updated_at)

		if err != nil {
			fmt.Println("Error in scanning the row" , err)
			return nil ,err
		}
		roles = append(roles, role)
	}
	return roles , nil 
}

func (u *UserRoleRepositoryImpl) AssignRoleToUser(userId int64 , roleId int64) error {
	query := `INSERT INTO USER_ROLE (USER_ID , ROLE_ID) VALUES ( ? , ?);`

	_ , err := u.db.Exec(query , userId , roleId)

	if err != nil {
		fmt.Println("Error executing query" , err)
		return err
	}
	return nil 
}

func (u *UserRoleRepositoryImpl) RemoveRoleFromUser(userId int64 , roleId int64) error {
	query := `DELETE FROM USER_ROLE WHERE USER_ID = ? AND ROLE_ID = ?;`

	_ , err := u.db.Exec(query , userId , roleId)
	
	if err != nil {
		fmt.Println("Error executing query" , err)
		return err
	}
	return nil 
}

func (u *UserRoleRepositoryImpl) GetUserPermissions(userId int64) ([]*models.Permission , error){
	query := `SELECT P.NAME , P.DESCRIPTION , P.RESOURCE , P.ACTION , P.CREATED_AT , P.UPDATED_AT
				FROM USER_ROLE UR 
				INNER JOIN ROLE_PERMISSION RP ON UR.ROLE_ID = RP.ROLE_ID
				INNER JOIN PERMISSION P ON RP.PERMISSION_ID = P.ID
				WHERE UR.USER_ID = ?;`
	
	rows , err := u.db.Query(query , userId)
	if err != nil {
		if err == sql.ErrNoRows {
			fmt.Println("No permission found for particular user id" , err)
		} else {
			fmt.Println("Error in quering" , err)
		}
		return nil , err
	}

	defer rows.Close()

	var permissions []*models.Permission
	
	for rows.Next() {
		permission := &models.Permission{}
		err := rows.Scan(&permission.Id , &permission.Name , &permission.Description , &permission.Resource , &permission.Action , 
		&permission.CreatedAt , &permission.UpdatedAt)

		if err != nil {
			fmt.Println("Error in scanning the row" , err)
			return nil ,err
		}
		permissions = append(permissions, permission)
	}
	return permissions , nil
}

func (u *UserRoleRepositoryImpl) HasPermission(userId int64 , permissionName string) (bool , error) {
	query := `SELECT COUNT(*) > 0
				FROM USER_ROLE UR
				INNER JOIN ROLE_PERMISSION RP ON RP.ROLE_ID = UR.ROLE_ID
				INNER JOIN PERMISSION P ON P.ID = RP.PERMISSION_ID
				WHERE UR.USER_ID = ? AND P.NAME = ?;`
	
	var exists bool 
	err := u.db.QueryRow(query , userId , permissionName).Scan(&exists)

	if err != nil {
		fmt.Println("Given Permission doesn't associate with user")
		return false , err
	}
	return exists , nil 
}

func (u *UserRoleRepositoryImpl) HasRole(userId int64, roleName string) (bool, error) {
	query := `SELECT COUNT(*)
				FROM USER_ROLE UR
				INNER JOIN ROLE R UR.ROLE_ID = R.ID
				WHERE USER_ROLE = ? AND ROLE.NAME = ?;`
	
	var exists bool ; 
	err := u.db.QueryRow(query , userId , roleName).Scan(&exists)
	if err != nil {
		fmt.Println("Given Role doesn't associate with user")
		return false, err
	}
	return exists, nil
}

func (u *UserRoleRepositoryImpl) HasAllRoles(userId int64, roleNames []string) (bool, error) {
	if len(roleNames) == 0 {
		return true , nil 
	}

	placeholders := make([]string , len(roleNames))
	args := make([]interface{} , len(roleNames) + 2)
	args[0] = len(roleNames)
	args[1] = userId

	for i , value := range roleNames {
		placeholders[i] = "?"
		args[i + 2] = value
	}

	query := `SELECT COUNT(*) = ?
				FROM USER_ROLE UR
				INNER JOIN ROLE R ON R.ID = UR.ROLE_ID
				WHERE UR.USER_ID = ? AND R.NAME IN (` + strings.Join(placeholders , ",") + `) ;`
	var exists bool 
	err := u.db.QueryRow(query , args...).Scan(&exists)

	if err != nil {
		fmt.Println("Error in quering" , err)
		return false , err
	}
	return exists , nil
}

func (u *UserRoleRepositoryImpl) HasAnyRole(userId int64 , roleNames []string) (bool, error) {
	if len(roleNames) == 0 {
		return true , nil 
	}
	placeholders := make([]string, len(roleNames))
	args := make([]interface{}, len(roleNames)+1)
	args[0] = userId
		
	for i, name := range roleNames {
		placeholders[i] = "?"
		args[i+1] = name
	}

	query := `SELECT COUNT(*) > 0 
				FROM USER_ROLE UR
				INNER JOIN ROLE R ON R.ID = UR.ROLE_ID
				WHERE UR.USER_ID = ? AND R.NAME IN (` + strings.Join(placeholders, ",") + `)`
	var exists bool 
	err := u.db.QueryRow(query , args...).Scan(&exists)

	if err != nil {
		fmt.Println("Error in quering" , err)
		return false , err
	}
	return exists , nil
}

================================================
FILE: AuthInGoService/dtos/auth.go
================================================
package dtos

type LoginUserRequest struct {
	Email string  `json:"email" validate:"required,email"`
	Password string `json:"password" validate:"required,min=8"`
}

type CreateUserRequest struct {
	Username string `json:"username" validate="required,min=3"`
	Email string  `json:"email" validate:"required,email"`
	Password string `json:"password" validate:"required,min=8"`
}

================================================
FILE: AuthInGoService/dtos/rbac.go
================================================
package dtos

type CreateRoleRequestDTO struct {
	Name        string `json:"name" validate:"required,min=2,max=50"`
	Description string `json:"description" validate:"required,min=5,max=200"`
}

type CreatePermissionRequestDTO struct {
	Name        string `json:"name" validate:"required,min=2,max=50"`
	Description string `json:"description" validate:"required,min=5,max=200"`
	Resource string `json:"resource" validate:"required,min=2,max=50"`
	Action string `json:"action" validate:"required,min=2,max=50"`
}

type UpdateRoleRequestDTO struct {
	Name        string `json:"name" validate:"required,min=2,max=50"`
	Description string `json:"description" validate:"required,min=5,max=200"`
}

type AssignPermissionRequestDTO struct {
	PermissionId int64 `json:"permission_id" validate:"required"`
}

type RemovePermissionRequestDTO struct {
	PermissionId int64 `json:"permission_id" validate:"required"`
}

================================================
FILE: AuthInGoService/main.go
================================================
package main

import (
	"AuthInGo/app"
	config "AuthInGo/config/env"
	dbConfig "AuthInGo/config/db"
)

func main(){
	config.Load() 

	cfg := app.NewConfig()
	dbConfig.InitDB()

	app := app.NewApplication(cfg)
	app.Run() ; 
}

================================================
FILE: AuthInGoService/middlewares/auth.go
================================================
package middlewares

import (
	config "AuthInGo/config/db"
	env "AuthInGo/config/env"
	db "AuthInGo/db/repositories"
	"context"
	"net/http"
	"strconv"
	"strings"

	"github.com/golang-jwt/jwt/v5"
)

func JWTMiddleware(next http.Handler) http.Handler{
	return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
		authHeaders := r.Header.Get("Authorization")

		if authHeaders == "" {
			http.Error(w, "Authorization header is required", http.StatusUnauthorized)
			return
		}

		if !strings.HasPrefix(authHeaders , "Bearer ") {
			http.Error(w, "Authorization header must start with Bearer", http.StatusUnauthorized)
			return
		}

		token := strings.TrimPrefix(authHeaders , "Bearer ")

		if token == "" {
			http.Error(w, "Token is required", http.StatusUnauthorized)
			return
		}

		claims := jwt.MapClaims{}
		parsedToken , err := jwt.ParseWithClaims(token , &claims , func(t *jwt.Token) (interface{}, error) {
			return []byte(env.GetString("JWT_SECRET" , "SECRET")) , nil
		})

		 if err != nil || !parsedToken.Valid {
            http.Error(w, "Invalid token", http.StatusUnauthorized)
            return
        }

		userId , okId := claims["id"].(float64)
		email , okEmail := claims["email"].(string)

		if !okId || !okEmail {
			http.Error(w, "Invalid token claims", http.StatusUnauthorized)
			return
		}

		ctx := context.WithValue(r.Context() , "userId" , strconv.Itoa(int(userId)))
		ctx = context.WithValue(ctx , "email" , email)
		next.ServeHTTP(w , r.WithContext(ctx))
	})
}

func RequireAllRoles(roles ...string) func(http.Handler) http.Handler {
	return func(next http.Handler) http.Handler {
		return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
			userId := r.Context().Value("userId").(string)

			userIdInt , _ := strconv.Atoi(userId)

			urr := db.NewUserRoleRepository(config.DB)

			hasAllRole , err :=  urr.HasAllRoles(int64(userIdInt) , roles)

			if err != nil {
				http.Error(w, "Error checking user roles: "+ err.Error(), http.StatusInternalServerError)
				return
			}

			if !hasAllRole {
				http.Error(w, "Forbidden: You do not have the required roles", http.StatusForbidden)
				return
			}
			next.ServeHTTP(w , r)
		})
	}
}

func RequireAnyRoles(roles ...string) func(http.Handler) http.Handler {
	return func(next http.Handler) http.Handler {
		return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
			userId := r.Context().Value("userId").(string)

			userIdInt , _ := strconv.Atoi(userId)

			urr := db.NewUserRoleRepository(config.DB)

			hasAllRole , err :=  urr.HasAnyRole(int64(userIdInt) , roles)

			if err != nil {
				http.Error(w, "Error checking user roles: "+ err.Error(), http.StatusInternalServerError)
				return
			}

			if !hasAllRole {
				http.Error(w, "Forbidden: You do not have the required roles", http.StatusForbidden)
				return
			}
			next.ServeHTTP(w , r)
		})
	}
}

================================================
FILE: AuthInGoService/middlewares/rate_limiter.go
================================================
package middlewares

import (
	"AuthInGo/utils"
	"errors"
	"net/http"

	"golang.org/x/time/rate"
)

func RateLimiter(next http.Handler) http.Handler {
	limiter := rate.NewLimiter(5 , 5)
	return http.HandlerFunc(func(w http.ResponseWriter , r *http.Request) {
		if !limiter.Allow(){
			utils.WriteErrorJsonResponse(w , "Too many Request" , http.StatusTooManyRequests , errors.New("Request Reached"))
			return 
		}
		next.ServeHTTP(w , r)
	})
}

================================================
FILE: AuthInGoService/middlewares/validator.go
================================================
package middlewares

import (
	"AuthInGo/dtos"
	"AuthInGo/utils"
	"context"
	"fmt"
	"net/http"
)

func ValidateRequestBody[T any](next http.Handler) http.Handler {
	return http.HandlerFunc(func(w http.ResponseWriter , r *http.Request){
		var payload T
		if jsonErr := utils.ReadJsonBody(r , &payload) ; jsonErr != nil {
			utils.WriteErrorJsonResponse(w , "JSON Reading Error" , http.StatusInternalServerError , jsonErr)
			return 
		}
		fmt.Println(payload)
		if validateErr := utils.Validator.Struct(payload) ; validateErr != nil {
			utils.WriteErrorJsonResponse(w , "Validation Failed" , http.StatusNotAcceptable , validateErr)
			return 
		}
		
		ctx := context.WithValue(r.Context() , "validatedPayload" , payload)
		next.ServeHTTP(w ,r.WithContext(ctx))
	})
}


func UserLoginRequestValidator(next http.Handler) http.Handler {
	return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
		var payload dtos.LoginUserRequest

		// Read and decode the JSON body into the payload
		if err := utils.ReadJsonBody(r, &payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Invalid request body", http.StatusBadRequest, err)
			return
		}

		// Validate the payload using the Validator instance
		if err := utils.Validator.Struct(payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Validation failed", http.StatusBadRequest, err)
			return
		}

		fmt.Println("Payload received for login:", payload)

		ctx := context.WithValue(r.Context(), "payload", payload) // Create a new context with the payload

		next.ServeHTTP(w, r.WithContext(ctx)) // Call the next handler in the chain
	})
}

func UserCreateRequestValidator(next http.Handler) http.Handler {
	return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
		var payload dtos.CreateUserRequest

		// Read and decode the JSON body into the payload
		if err := utils.ReadJsonBody(r, &payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Invalid request body", http.StatusBadRequest, err)
			return
		}

		// Validate the payload using the Validator instance
		if err := utils.Validator.Struct(payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Validation failed", http.StatusBadRequest, err)
			return
		}

		ctx := context.WithValue(r.Context(), "payload", payload)

		next.ServeHTTP(w, r.WithContext(ctx)) // Call the next handler in the chain
	})
}

func CreateRoleRequestValidator(next http.Handler) http.Handler {
	return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
		var payload dtos.CreateRoleRequestDTO

		// Read and decode the JSON body into the payload
		if err := utils.ReadJsonBody(r, &payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Invalid request body", http.StatusBadRequest, err)
			return
		}

		// Validate the payload using the Validator instance
		if err := utils.Validator.Struct(payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Validation failed", http.StatusBadRequest, err)
			return
		}

		ctx := context.WithValue(r.Context(), "payload", payload)

		next.ServeHTTP(w, r.WithContext(ctx))
	})
}

func UpdateRoleRequestValidator(next http.Handler) http.Handler {
	return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
		var payload dtos.UpdateRoleRequestDTO

		// Read and decode the JSON body into the payload
		if err := utils.ReadJsonBody(r, &payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Invalid request body", http.StatusBadRequest, err)
			return
		}

		// Validate the payload using the Validator instance
		if err := utils.Validator.Struct(payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Validation failed", http.StatusBadRequest, err)
			return
		}

		ctx := context.WithValue(r.Context(), "payload", payload)

		next.ServeHTTP(w, r.WithContext(ctx))
	})
}

func AssignPermissionRequestValidator(next http.Handler) http.Handler {
	return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
		var payload dtos.AssignPermissionRequestDTO

		// Read and decode the JSON body into the payload
		if err := utils.ReadJsonBody(r, &payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Invalid request body", http.StatusBadRequest, err)
			return
		}

		// Validate the payload using the Validator instance
		if err := utils.Validator.Struct(payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Validation failed", http.StatusBadRequest, err)
			return
		}

		ctx := context.WithValue(r.Context(), "payload", payload)

		next.ServeHTTP(w, r.WithContext(ctx))
	})
}

func RemovePermissionRequestValidator(next http.Handler) http.Handler {
	return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
		var payload dtos.RemovePermissionRequestDTO

		// Read and decode the JSON body into the payload
		if err := utils.ReadJsonBody(r, &payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Invalid request body", http.StatusBadRequest, err)
			return
		}

		// Validate the payload using the Validator instance
		if err := utils.Validator.Struct(payload); err != nil {
			utils.WriteErrorJsonResponse(w, "Validation failed", http.StatusBadRequest, err)
			return
		}

		ctx := context.WithValue(r.Context(), "payload", payload)

		next.ServeHTTP(w, r.WithContext(ctx))
	})
}

================================================
FILE: AuthInGoService/models/rbac.go
================================================
package models

type Role struct {
	Id int64
	Name string  
	Description string 
	Created_at string 
	Updated_at string
}

type Permission struct {
	Id          int64
	Name        string
	Description string
	Resource    string
	Action      string
	CreatedAt   string
	UpdatedAt   string
}

type RolePermission struct {
	Id           int64
	RoleId       int64
	PermissionId int64
	CreatedAt    string
	UpdatedAt    string
}

================================================
FILE: AuthInGoService/models/user.go
================================================
package models

type User struct {
	Id        int64
	Username  string
	Email     string
	Password  string
	CreatedAt string
	UpdatedAt string
}


================================================
FILE: AuthInGoService/routers/permission_router.go
================================================
package routers

import (
	"AuthInGo/controllers"

	"github.com/go-chi/chi/v5"
)

type PermissionRouter struct {
	permissionController *controllers.PermissionController
}

func NewPermissionRouter(_permissionController *controllers.PermissionController) Router {
	return &PermissionRouter{
		permissionController: _permissionController,
	}
}

func (rr *PermissionRouter) Register(r chi.Router){
	r.Get("/permission/{id}" , rr.permissionController.GetPermissionById)
	r.Get("/permission" , rr.permissionController.GetPermissionByName)
	r.Post("/permission" , rr.permissionController.CreatePermission)
	r.Delete("/permission/{id}" , rr.permissionController.DeleteById)
	r.Put("/permission/{id}" , rr.permissionController.UpdateById)
}


================================================
FILE: AuthInGoService/routers/role_router.go
================================================
package routers

import (
	"AuthInGo/controllers"
	"AuthInGo/middlewares"

	"github.com/go-chi/chi/v5"
)

type RoleRouter struct {
	roleController *controllers.RoleController
}

func NewRoleRouter(_roleController *controllers.RoleController) Router {
	return &RoleRouter{
		roleController: _roleController,
	}
}

func (rr *RoleRouter) Register(r chi.Router){
	r.Get("/role/{id}" , rr.roleController.GetRoleById)
	r.Get("/role" , rr.roleController.GetRoleByName) 
	r.With(middlewares.CreateRoleRequestValidator).Post("/role" , rr.roleController.CreateRole)
	r.Delete("/role/{id}" , rr.roleController.DeleteById)
	r.With(middlewares.UpdateRoleRequestValidator).Put("/role/{id}" , rr.roleController.UpdateById)

	r.Get("/role/{id}/permissions", rr.roleController.GetRolePermissions)
	r.With(middlewares.AssignPermissionRequestValidator).Post("/role/{id}/permissions", rr.roleController.AssignPermissionToRole)
	r.With(middlewares.RemovePermissionRequestValidator).Delete("/role/{id}/permissions", rr.roleController.RemovePermissionFromRole)
	r.Get("/role-permissions", rr.roleController.GetAllRolePermissions)
	r.With(middlewares.JWTMiddleware , middlewares.RequireAllRoles("admin")).Post("/role/{userId}/assign/{roleId}", rr.roleController.AssignRoleToUser)
}

================================================
FILE: AuthInGoService/routers/router.go
================================================
package routers

import (
	"AuthInGo/controllers"
	"AuthInGo/middlewares"
