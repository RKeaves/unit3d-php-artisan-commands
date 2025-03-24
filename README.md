# Unit3D php-artisan commands reference

A comprehensive list of PHP artisan commands for Unit3D tracker management.

## Table of Contents
- [Basic Commands](#basic-commands)
- [Achievements](#achievements)
- [Authentication](#authentication)
- [Automation](#automation)
- [Backup](#backup)
- [Cache](#cache)
- [Database](#database)
- [Debug](#debug)
- [Maintenance](#maintenance)
- [Make Commands](#make-commands)
- [Queue](#queue)
- [Scout](#scout)
- [Full List](#full-list)

---

## Basic Commands

```bash
php artisan about
```
_Display application information_

---
```bash
php artisan serve
```
_Start development server_

---
```bash
php artisan tinker
```
_Interactive shell_

---
```bash
php artisan migrate
```
_Run database migrations_

---
```bash
php artisan optimize
```
_Cache framework files_

---
```bash
php artisan down
```
_Enter maintenance mode_

---
```bash
php artisan up
```
_Exit maintenance mode_

---

## Achievements

```bash
php artisan achievements:load
```
_Load achievements to database_

---

## Authentication

```bash
php artisan auth:clear-resets
```
_Flush expired password resets_

---

## Automation

```bash
php artisan auto:ban_disposable_users
```
_Ban disposable email users_

---
```bash
php artisan auto:bon_allocation
```
_Allocate bonus points_

---
```bash
php artisan auto:cache_random_media
```
_Cache random media IDs_

---
```bash
php artisan auto:correct_history
```
_Fix stuck active records_

---
```bash
php artisan auto:deactivate_warning
```
_Deactivate expired warnings_

---
```bash
php artisan auto:delete_stopped_peers
```
_Remove stopped peers_

---
```bash
php artisan auto:disable_inactive_users
```
_Disable inactive accounts_

---
```bash
php artisan auto:email-blacklist-update
```
_Update email blacklist_

---
```bash
php artisan auto:group
```
_Auto-update user groups_

---
```bash
php artisan auto:highspeed_tag
```
_Update seedbox tags_

---
```bash
php artisan auto:refund_download
```
_Refund downloads by seedtime_

---
```bash
php artisan auto:remove_featured_torrent
```
_Remove expired featured torrents_

---
```bash
php artisan auto:sync_peers
```
_Sync peer counts_

---
```bash
php artisan auto:sync_torrents_to_meilisearch
```
_Sync to search index_

---

## Backup

```bash
php artisan backup:clean
```
_Clean old backups_

---
```bash
php artisan backup:list
```
_List backups_

---
```bash
php artisan backup:run
```
_Create new backup_

---

## Cache

```bash
php artisan cache:clear
```
_Clear application cache_

---
```bash
php artisan clear:all_cache
```
_Clear all caches_

---
```bash
php artisan set:all_cache
```
_Set common caches_

---

## Database

```bash
php artisan db:seed
```
_Seed database_

---
```bash
php artisan db:wipe
```
_Drop all tables_

---
```bash
php artisan migrate:fresh
```
_Run fresh migrations_

---

## Debug

```bash
php artisan auto:flush_peers
```
_Flush ghost peers_

---
```bash
php artisan auto:recycle_invites
```
_Recycle expired invites_

---
```bash
php artisan auto:remove_expired_donors
```
_Remove expired donors_

---
```bash
php artisan auto:reset_user_flushes
```
_Reset peer flush limits_

---
```bash
php artisan tickets:stale
```
_Check stale tickets_

---

## Maintenance

```bash
php artisan auto:flush_peers
```
_Flush ghost peers_

---
```bash
php artisan auto:recycle_invites
```
_Recycle expired invites_

---
```bash
php artisan auto:remove_expired_donors
```
_Remove expired donors_

---
```bash
php artisan auto:reset_user_flushes
```
_Reset peer flush limits_

---
```bash
php artisan tickets:stale
```
_Check stale tickets_

---

## Make Commands

```bash
php artisan make:model
```
_Create new model_

---
```bash
php artisan make:controller
```
_Create new controller_

---
```bash
php artisan make:migration
```
_Create new migration_

---
```bash
php artisan make:middleware
```
_Create new middleware_

---

## Queue

```bash
php artisan queue:work
```
_Process jobs_

---
```bash
php artisan queue:retry
```
_Retry failed jobs_

---
```bash
php artisan queue:monitor
```
_Monitor queue sizes_

---

## Scout

```bash
php artisan scout:import
```
_Import models to search_

---
```bash
php artisan scout:flush
```
_Flush model records_

---
```bash
php artisan scout:index
```
_Create search index_

---

## Full List

Below is the full list of available artisan commands. Each command is provided in its own code block with a horizontal rule (---) between each entry for clarity.

```bash
about
```
_Display basic information about your application_
---
```bash
clear-compiled
```
_Remove the compiled class file_
---
```bash
completion
```
_Dump the shell completion script_
---
```bash
db
```
_Start a new database CLI session_
---
```bash
docs
```
_Access the Laravel documentation_
---
```bash
down
```
_Put the application into maintenance/demo mode_
---
```bash
env
```
_Display the current framework environment_
---
```bash
help
```
_Display help for a command_
---
```bash
list
```
_List commands_
---
```bash
migrate
```
_Run the database migrations_
---
```bash
optimize
```
_Cache framework bootstrap, configuration, and metadata to increase performance_
---
```bash
serve
```
_Serve the application on the PHP development server_
---
```bash
test
```
_Run the application tests_
---
```bash
tinker
```
_Interact with your application_
---
```bash
up
```
_Bring the application out of maintenance mode_
---
```bash
achievements:load
```
_Load all Achievements to database_
---
```bash
auth:clear-resets
```
_Flush expired password reset tokens_
---
```bash
auto:ban_disposable_users
```
_Ban user if using a disposable email_
---
```bash
auto:bon_allocation
```
_Allocates bonus points to users based on peer activity_
---
```bash
auto:cache_random_media
```
_Caches valid media IDs for random media component_
---
```bash
auto:cache_user_leech_counts
```
_Caches user leech counts_
---
```bash
auto:correct_history
```
_Corrects history records that appear active despite not receiving a STOPPED event from the client_
---
```bash
auto:deactivate_warning
```
_Automatically deactivates user warnings if expired_
---
```bash
auto:delete_stopped_peers
```
_Deletes all stopped peers_
---
```bash
auto:delete_unparticipated_conversations
```
_Deletes conversations where all users have deleted their participation_
---
```bash
auto:disable_inactive_users
```
_Disables inactive user accounts based on criteria_
---
```bash
auto:email-blacklist-update
```
_Updates the cache for email domains blacklist_
---
```bash
auto:flush_peers
```
_Flushes ghost peers_
---
```bash
auto:group
```
_Automatically changes a user’s group class if requirements are met_
---
```bash
auto:highspeed_tag
```
_Updates torrents’ highspeed tag based on registered seedboxes_
---
```bash
auto:nerdstat
```
_Automatically posts daily nerd stats to the shoutbox_
---
```bash
auto:prewarning
```
_Automatically sends pre-warning notifications to users_
---
```bash
auto:recycle_audits
```
_Recycles audits once they are X days old_
---
```bash
auto:recycle_claimed_torrent_requests
```
_Recycles torrent requests that were claimed but not filled within 7 days_
---
```bash
auto:recycle_failed_logins
```
_Recycles failed logins once 30 days old_
---
```bash
auto:recycle_invites
```
_Recycles expired invites_
---
```bash
auto:refund_download
```
_Refunds download credits to users based on seed time_
---
```bash
auto:remove_expired_donors
```
_Automatically removes expired donors_
---
```bash
auto:remove_featured_torrent
```
_Automatically removes featured torrents if expired_
---
```bash
auto:remove_personal_freeleech
```
_Automatically removes a user’s personal freeleech if it has expired_
---
```bash
auto:remove_torrent_buffs
```
_Automatically removes torrent buffs if expired_
---
```bash
auto:reset_user_flushes
```
_Resets the daily limit for users to flush their own peers_
---
```bash
auto:reward_resurrection
```
_Automatically hands out rewards for successful resurrections_
---
```bash
auto:softdelete_disabled_users
```
_Disables users in a disabled group for a specified period_
---
```bash
auto:sync_peers
```
_Syncs torrent seeders, leechers, and times completed count_
---
```bash
auto:sync_people_to_meilisearch
```
_Syncs people to Meilisearch_
---
```bash
auto:sync_torrent_season_episode
```
_Syncs season and episode numbers from torrent titles to the database_
---
```bash
auto:sync_torrents_to_meilisearch
```
_Syncs torrents and their relations to Meilisearch_
---
```bash
auto:torrent_balance
```
_Calculates balance for all torrents_
---
```bash
auto:update_user_last_actions
```
_Updates user last actions in batches_
---
```bash
auto:upsert_announces
```
_Upserts announces in batches_
---
```bash
auto:upsert_histories
```
_Upserts peer histories in batches_
---
```bash
auto:upsert_peers
```
_Upserts peers in batches_
---
```bash
auto:warning
```
_Automatically posts warnings to users’ accounts and warnings table_
---
```bash
backup:clean
```
_Removes all backups older than the specified number of days_
---
```bash
backup:list
```
_Displays a list of all backups_
---
```bash
backup:monitor
```
_Monitors the health of all backups_
---
```bash
backup:run
```
_Runs the backup process_
---
```bash
cache:clear
```
_Flushes the application cache_
---
```bash
cache:forget
```
_Removes an item from the cache_
---
```bash
cache:prune-stale-tags
```
_Prunes stale cache tags from the cache (Redis only)_
---
```bash
channel:list
```
_Lists all registered private broadcast channels_
---
```bash
clean:torrent_files
```
_Cleans torrent files to remove extra unneeded data_
---
```bash
clear:all_cache
```
_Clears several common caches_
---
```bash
config:cache
```
_Creates a cache file for faster configuration loading_
---
```bash
config:clear
```
_Removes the configuration cache file_
---
```bash
config:publish
```
_Publishes configuration files to your application_
---
```bash
config:show
```
_Displays all values for a given configuration file or key_
---
```bash
db:monitor
```
_Monitors the number of connections on the specified database_
---
```bash
db:seed
```
_Seeds the database with records_
---
```bash
db:show
```
_Displays information about the given database_
---
```bash
db:table
```
_Displays information about the given database table_
---
```bash
db:wipe
```
_Drops all tables, views, and types_
---
```bash
debugbar:clear
```
_Clears the Debugbar storage_
---
```bash
demo:seed
```
_Seeds fake data for demonstration or testing purposes_
---
```bash
env:decrypt
```
_Decrypts an environment file_
---
```bash
env:encrypt
```
_Encrypts an environment file_
---
```bash
event:cache
```
_Discovers and caches the application's events and listeners_
---
```bash
event:clear
```
_Clears all cached events and listeners_
---
```bash
event:list
```
_Lists the application's events and listeners_
---
```bash
fetch:meta
```
_Fetches meta data for new systems on preexisting torrents_
---
```bash
git:update
```
_Executes commands necessary to update your website using Git_
---
```bash
igdb:publish
```
_Publishes IGDB-Laravel configuration_
---
```bash
igdb:webhooks
```
_Lists all your registered webhooks at IGDB_
---
```bash
igdb:webhooks:create
```
_Creates a webhook at IGDB_
---
```bash
igdb:webhooks:delete
```
_Deletes a webhook at IGDB_
---
```bash
igdb:webhooks:reactivate
```
_Reactivates an inactive webhook_
---
```bash
install:api
```
_Creates an API routes file and installs Laravel Sanctum or Laravel Passport_
---
```bash
install:broadcasting
```
_Creates a broadcasting channel routes file_
---
```bash
irc:message
```
_Sends a message to an IRC channel_
---
```bash
key:generate
```
_Sets the application key_
---
```bash
lang:publish
```
_Publishes all language files available for customization_
---
```bash
livewire:attribute
```
_Creates a new Livewire attribute class_
---
```bash
livewire:configure-s3-upload-cleanup
```
_Configures S3 temporary file upload cleanup for files older than 24 hours_
---
```bash
livewire:copy
```
_Copies a Livewire component_
---
```bash
livewire:delete
```
_Deletes a Livewire component_
---
```bash
livewire:form
```
_Creates a new Livewire form class_
---
```bash
livewire:layout
```
_Creates a new app layout file_
---
```bash
livewire:make
```
_Creates a new Livewire component_
---
```bash
livewire:move
```
_Moves a Livewire component_
---
```bash
livewire:publish
```
_Publishes Livewire configuration_
---
```bash
livewire:stubs
```
_Publishes Livewire stubs_
---
```bash
livewire:upgrade
```
_Interactive upgrade helper to migrate from v2 to v3_
---
```bash
make:achievement
```
_Creates a new achievement class_
---
```bash
make:achievement_chain
```
_Creates a new achievement chain class_
---
```bash
make:cache-table
```
_Creates a migration for the cache database table_
---
```bash
make:cast
```
_Creates a new custom Eloquent cast class_
---
```bash
make:channel
```
_Creates a new channel class_
---
```bash
make:class
```
_Creates a new class_
---
```bash
make:command
```
_Creates a new Artisan command_
---
```bash
make:component
```
_Creates a new view component class_
---
```bash
make:controller
```
_Creates a new controller class_
---
```bash
make:enum
```
_Creates a new enum_
---
```bash
make:event
```
_Creates a new event class_
---
```bash
make:exception
```
_Creates a new custom exception class_
---
```bash
make:factory
```
_Creates a new model factory_
---
```bash
make:interface
```
_Creates a new interface_
---
```bash
make:job
```
_Creates a new job class_
---
```bash
make:job-middleware
```
_Creates a new job middleware class_
---
```bash
make:listener
```
_Creates a new event listener class_
---
```bash
make:livewire
```
_Creates a new Livewire component_
---
```bash
make:mail
```
_Creates a new email class_
---
```bash
make:middleware
```
_Creates a new HTTP middleware class_
---
```bash
make:migration
```
_Creates a new migration file_
---
```bash
make:model
```
_Creates a new Eloquent model class_
---
```bash
make:notification
```
_Creates a new notification class_
---
```bash
make:notifications-table
```
_Creates a migration for the notifications table_
---
```bash
make:observer
```
_Creates a new observer class_
---
```bash
make:policy
```
_Creates a new policy class_
---
```bash
make:provider
```
_Creates a new service provider class_
---
```bash
make:queue-batches-table
```
_Creates a migration for the batches database table_
---
```bash
make:queue-failed-table
```
_Creates a migration for the failed queue jobs database table_
---
```bash
make:queue-table
```
_Creates a migration for the queue jobs database table_
---
```bash
make:request
```
_Creates a new form request class_
---
```bash
make:resource
```
_Creates a new resource_
---
```bash
make:rule
```
_Creates a new validation rule_
---
```bash
make:scope
```
_Creates a new scope class_
---
```bash
make:seeder
```
_Creates a new seeder class_
---
```bash
make:session-table
```
_Creates a migration for the session database table_
---
```bash
make:test
```
_Creates a new test class_
---
```bash
make:trait
```
_Creates a new trait_
---
```bash
make:view
```
_Creates a new view_
---
```bash
migrate:fresh
```
_Drops all tables and re-runs all migrations_
---
```bash
migrate:install
```
_Creates the migration repository_
---
```bash
migrate:refresh
```
_Resets and re-runs all migrations_
---
```bash
migrate:reset
```
_Rolls back all database migrations_
---
```bash
migrate:rollback
```
_Rolls back the last database migration_
---
```bash
migrate:status
```
_Shows the status of each migration_
---
```bash
model:prune
```
_Prunes models that are no longer needed_
---
```bash
model:show
```
_Shows information about an Eloquent model_
---
```bash
octane:install
```
_Installs the Octane components and resources_
---
```bash
octane:reload
```
_Reloads the Octane workers_
---
```bash
octane:start
```
_Starts the Octane server_
---
```bash
octane:status
```
_Gets the current status of the Octane server_
---
```bash
octane:stop
```
_Stops the Octane server_
---
```bash
optimize:clear
```
_Removes the cached bootstrap files_
---
```bash
package:discover
```
_Rebuilds the cached package manifest_
---
```bash
pest:dataset
```
_Creates a new dataset file_
---
```bash
pest:test
```
_Creates a new test file_
---
```bash
queue:clear
```
_Deletes all jobs from the specified queue_
---
```bash
queue:failed
```
_Lists all failed queue jobs_
---
```bash
queue:flush
```
_Flushes all failed queue jobs_
---
```bash
queue:forget
```
_Deletes a failed queue job_
---
```bash
queue:listen
```
_Listens to a given queue_
---
```bash
queue:monitor
```
_Monitors the size of the specified queues_
---
```bash
queue:prune-batches
```
_Prunes stale entries from the batches database_
---
```bash
queue:prune-failed
```
_Prunes stale entries from the failed jobs table_
---
```bash
queue:restart
```
_Restarts queue worker daemons after their current job_
---
```bash
queue:retry
```
_Retries a failed queue job_
---
```bash
queue:retry-batch
```
_Retries the failed jobs for a batch_
---
```bash
queue:work
```
_Starts processing jobs on the queue as a daemon_
---
```bash
route:cache
```
_Creates a route cache file for faster route registration_
---
```bash
route:clear
```
_Removes the route cache file_
---
```bash
route:list
```
_Lists all registered routes_
---
```bash
sail:add
```
_Adds a service to an existing Sail installation_
---
```bash
sail:install
```
_Installs Laravel Sail’s default Docker Compose file_
---
```bash
sail:publish
```
_Publishes the Laravel Sail Docker files_
---
```bash
sail-ssl:install
```
_Installs the Nginx container in Docker Compose_
---
```bash
sail-ssl:publish
```
_Publishes the Nginx resources_
---
```bash
schedule:clear-cache
```
_Deletes the cached mutex files created by the scheduler_
---
```bash
schedule:interrupt
```
_Interrupts the current schedule run_
---
```bash
schedule:list
```
_Lists all scheduled tasks_
---
```bash
schedule:run
```
_Runs the scheduled commands_
---
```bash
schedule:test
```
_Runs a scheduled command_
---
```bash
schedule:work
```
_Starts the schedule worker_
---
```bash
schema:dump
```
_Dumps the given database schema_
---
```bash
scout:delete-all-indexes
```
_Deletes all indexes_
---
```bash
scout:delete-index
```
_Deletes an index_
---
```bash
scout:flush
```
_Flushes all of the model's records from the index_
---
```bash
scout:import
```
_Imports the given model into the search index_
---
```bash
scout:index
```
_Creates an index_
---
```bash
scout:sync-index-settings
```
_Syncs your configured index settings with your search engine (Meilisearch)_
---
```bash
set:all_cache
```
_Sets several common caches_
---
```bash
storage:link
```
_Creates the symbolic links configured for the application_
---
```bash
storage:unlink
```
_Deletes existing symbolic links configured for the application_
---
```bash
stub:publish
```
_Publishes all stubs available for customization_
---
```bash
test:email
```
_Sends a test email to the owner account using the current mail configuration_
---
```bash
tickets:stale
```
_Checks for tickets open longer than 3 days_
---
```bash
vendor:publish
```
_Publishes any publishable assets from vendor packages_
---
```bash
view:cache
```
_Compiles all of the application's Blade templates_
---
```bash
view:clear
```
_Clears all compiled view files_
 
