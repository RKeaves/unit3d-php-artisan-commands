# Unit3d php-artisan Commands Reference

<p align="center">
  <img src="https://ptpimg.me/6o8x8j.png" alt="Centered Image" style="width: 12%;">
</p>

<p align="center">
Master essential PHP Artisan commands to efficiently manage your Unit3D tracker.
</p>

> **Always test these commands on a staging or test server before using them in production.** Some commands can significantly alter data or disrupt service if not used correctly. Ensure you fully understand the purpose and impact of each command prior to execution.


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

> **Note:** Use this command to get a quick overview of your application’s version, environment, and installed packages. It’s a handy troubleshooting tool.

---
```bash
php artisan serve
```
_Start development server_

> **Tip:** Ideal for local development and testing. It starts a lightweight PHP server, but remember to use a robust web server (like Apache or Nginx) for production.

---
```bash
php artisan tinker
```
_Interactive shell_

> **Tip:** Provides an interactive REPL for your Laravel application. Use it to experiment with your code, run quick tests, or debug without creating dedicated scripts.

---
```bash
php artisan migrate
```
_Run database migrations_

> **Note:** Applies pending database migrations. Run this after modifying migration files to update your database schema. Always back up your data before performing migrations in production.

---
```bash
php artisan optimize
```
_Cache framework files_

> **Tip:** Improves performance by caching bootstrap files and configurations. Use this command when preparing your application for production deployment.

---
```bash
php artisan down
```
_Enter maintenance mode_

> **Note:** Puts your application into maintenance mode for updates. Visitors will see a maintenance message until you run the `up` command.

---
```bash
php artisan up
```
_Exit maintenance mode_

> **Tip:** Brings your application back online after maintenance. Always verify that your application is working as expected after exiting maintenance mode.

---

## Achievements

```bash
php artisan achievements:load
```
_Load achievements to database_

> **Note:** Imports or updates achievement data. Use this command when adding new achievements or updating existing ones to ensure your database is current.

---

## Authentication

```bash
php artisan auth:clear-resets
```
_Flush expired password resets_

> **Tip:** Clears outdated password reset tokens from your database. Run this regularly to keep the authentication system secure and efficient.

---

## Automation

```bash
php artisan auto:ban_disposable_users
```
_Ban disposable email users_

> **Note:** Automatically bans users registering with disposable email addresses. Use this to improve registration quality and reduce spam accounts.

---
```bash
php artisan auto:bon_allocation
```
_Allocate bonus points_

> **Tip:** Distributes bonus points based on peer activity. This is useful for gamifying user engagement and rewarding active participation.

---
```bash
php artisan auto:cache_random_media
```
_Cache random media IDs_

> **Note:** Pre-caches random media IDs to speed up access in components that display random content. Helpful for performance optimization.

---
```bash
php artisan auto:correct_history
```
_Fix stuck active records_

> **Tip:** Corrects historical records that remain active erroneously. Use this command if you notice inconsistencies in activity tracking.

---
```bash
php artisan auto:deactivate_warning
```
_Deactivate expired warnings_

> **Note:** Automatically deactivates warnings that have passed their expiration date. This keeps your user warning system current and relevant.

---
```bash
php artisan auto:delete_stopped_peers
```
_Remove stopped peers_

> **Tip:** Cleans up peer records that are no longer active. Use it to maintain accurate data on active connections.

---
```bash
php artisan auto:disable_inactive_users
```
_Disable inactive accounts_

> **Note:** Automatically disables user accounts that have been inactive for a specified period. Helps manage system load and security.

---
```bash
php artisan auto:email-blacklist-update
```
_Update email blacklist_

> **Tip:** Refreshes the email domain blacklist cache. Run this periodically to prevent signups from disreputable domains.

---
```bash
php artisan auto:group
```
_Auto-update user groups_

> **Note:** Automatically adjusts user groups based on predefined criteria. Useful for dynamically managing user permissions and roles.

---
```bash
php artisan auto:highspeed_tag
```
_Update seedbox tags_

> **Tip:** Updates torrent seedbox tags to reflect current status. Use this to keep torrent metadata accurate.

---
```bash
php artisan auto:refund_download
```
_Refund downloads by seedtime_

> **Note:** Processes refunds for downloads based on seed time. Essential for maintaining fairness in credit systems.

---
```bash
php artisan auto:remove_featured_torrent
```
_Remove expired featured torrents_

> **Tip:** Automatically removes torrents marked as featured once their expiry passes. Use this to keep your featured list fresh.

---
```bash
php artisan auto:sync_peers
```
_Sync peer counts_

> **Note:** Updates the counts of seeders and leechers for torrents. Critical for accurate torrent statistics.

---
```bash
php artisan auto:sync_torrents_to_meilisearch
```
_Sync to search index_

> **Tip:** Synchronizes torrent data with Meilisearch for improved search functionality. Run this after major data updates.

---

## Backup

```bash
php artisan backup:clean
```
_Clean old backups_

> **Note:** Removes outdated backups based on your configuration. Run this to conserve storage space and maintain backup hygiene.

---
```bash
php artisan backup:list
```
_List backups_

> **Tip:** Displays a list of all available backups. Use this to verify backup schedules and integrity.

---
```bash
php artisan backup:run
```
_Create new backup_

> **Note:** Generates a new backup of your application and database. It’s a critical step before making major changes or deployments.

---

## Cache

```bash
php artisan cache:clear
```
_Clear application cache_

> **Tip:** Removes cached data to ensure that changes are reflected immediately. Use this when you update configuration or view files.

---
```bash
php artisan clear:all_cache
```
_Clear all caches_

> **Note:** Clears various caches used by the application. This is useful when troubleshooting caching issues across multiple components.

---
```bash
php artisan set:all_cache
```
_Set common caches_

> **Tip:** Pre-sets commonly used caches to boost performance. Run this command after clearing caches to restore optimal settings.

---

## Database

```bash
php artisan db:seed
```
_Seed database_

> **Note:** Populates the database with initial or test data. Use this command after running migrations or when setting up a fresh instance.

---
```bash
php artisan db:wipe
```
_Drop all tables_

> **Tip:** Completely clears the database by dropping all tables. Use this with caution, ideally in a development environment.

---
```bash
php artisan migrate:fresh
```
_Run fresh migrations_

> **Note:** Drops all tables and re-runs all migrations. Ideal for resetting the database during development or testing.

---

## Debug

```bash
php artisan auto:flush_peers
```
_Flush ghost peers_

> **Tip:** Clears inactive peer connections to maintain accurate statistics. Use this regularly during peak usage periods.

---
```bash
php artisan auto:recycle_invites
```
_Recycle expired invites_

> **Note:** Processes and recycles invites that have expired. Helps manage invitation systems effectively.
 
---
```bash
php artisan auto:remove_expired_donors
```
_Remove expired donors_

> **Tip:** Automatically removes donor statuses that are no longer valid. Use this to keep donor records up-to-date.

---
```bash
php artisan auto:reset_user_flushes
```
_Reset peer flush limits_

> **Note:** Resets daily limits for users to flush their own peers. Useful in maintaining system limits and preventing abuse.

---
```bash
php artisan tickets:stale
```
_Check stale tickets_

> **Tip:** Identifies and flags tickets that have been open too long. Run this periodically to ensure timely ticket resolution.

---

## Maintenance

```bash
php artisan auto:flush_peers
```
_Flush ghost peers_

> **Note:** Same as in Debug, used to clean up inactive connections during maintenance windows.

---
```bash
php artisan auto:recycle_invites
```
_Recycle expired invites_

> **Tip:** Run this before major maintenance tasks to ensure no outdated invites are pending.
 
---
```bash
php artisan auto:remove_expired_donors
```
_Remove expired donors_

> **Note:** Keeps donor data current; run this as part of routine maintenance.
 
---
```bash
php artisan auto:reset_user_flushes
```
_Reset peer flush limits_

> **Tip:** Use this command during scheduled maintenance to reset system limits without manual intervention.
 
---
```bash
php artisan tickets:stale
```
_Check stale tickets_

> **Note:** Verify and clear outdated tickets to ensure support workflows remain efficient.

---

## Make Commands

```bash
php artisan make:model
```
_Create new model_

> **Tip:** Generates an Eloquent model file. Use this when you need to create a new database model with basic structure.

---
```bash
php artisan make:controller
```
_Create new controller_

> **Note:** Generates a controller file for handling HTTP requests. Ideal for setting up new application logic endpoints.

---
```bash
php artisan make:migration
```
_Create new migration_

> **Tip:** Creates a new migration file to modify your database schema. Always review and adjust the generated file before running migrations.

---
```bash
php artisan make:middleware
```
_Create new middleware_

> **Note:** Generates a middleware class for request filtering. Use this to add custom logic for processing HTTP requests.

---

## Queue

```bash
php artisan queue:work
```
_Process jobs_

> **Tip:** Starts processing jobs in the queue continuously. Best used in production with a dedicated worker process.

---
```bash
php artisan queue:retry
```
_Retry failed jobs_

> **Note:** Retries jobs that previously failed. Use this to handle transient issues or after resolving underlying errors.
 
---
```bash
php artisan queue:monitor
```
_Monitor queue sizes_

> **Tip:** Displays current queue statistics. Helps in scaling workers or diagnosing delays.

---

## Scout

```bash
php artisan scout:import
```
_Import models to search_

> **Note:** Imports data for models into your search index (e.g., Meilisearch). Run this after updating your models or schema.

---
```bash
php artisan scout:flush
```
_Flush model records_

> **Tip:** Clears all indexed records for a model. Use it before a full re-index to avoid duplicates.
 
---
```bash
php artisan scout:index
```
_Create search index_

> **Note:** Creates a new search index for your model. Ensure your search engine is configured properly before using this command.

---

## Full List

Below is the full list of available artisan commands with detailed descriptions and notes. Each entry is separated by a horizontal rule for clarity.

```bash
about
```
_Display basic information about your application_

> **Tip:** Quickly verify the current application version and configuration.

---
```bash
clear-compiled
```
_Remove the compiled class file_

> **Note:** Useful when you need to clear cached classes after code changes.

---
```bash
completion
```
_Dump the shell completion script_

> **Tip:** Generate a completion script for your shell to speed up command-line usage.
 
---
```bash
db
```
_Start a new database CLI session_

> **Note:** Provides direct access to your database via Artisan. Use with caution.

---
```bash
docs
```
_Access the Laravel documentation_

> **Tip:** Opens the official Laravel docs. Great for quick reference when coding.

---
```bash
down
```
_Put the application into maintenance/demo mode_

> **Note:** Temporarily disable public access during updates or maintenance tasks.

---
```bash
env
```
_Display the current framework environment_

> **Tip:** Confirm which environment (development, production, etc.) your application is running in.

---
```bash
help
```
_Display help for a command_

> **Note:** Use this command to view detailed help and options for any Artisan command.
 
---
```bash
list
```
_List commands_

> **Tip:** Shows all available commands. A useful starting point if you’re not sure what’s available.
 
---
```bash
migrate
```
_Run the database migrations_

> **Note:** Applies pending migrations. Essential for updating your database schema.

---
```bash
optimize
```
_Cache framework bootstrap, configuration, and metadata to increase performance_

> **Tip:** Run this command before deployment to boost application performance.
 
---
```bash
serve
```
_Serve the application on the PHP development server_

> **Note:** Best suited for local development. Not recommended for production environments.
 
---
```bash
test
```
_Run the application tests_

> **Tip:** Execute your test suite to ensure code integrity after changes.
 
---
```bash
tinker
```
_Interact with your application_

> **Note:** Provides a REPL for experimenting with your Laravel application. Great for quick testing.
 
---
```bash
up
```
_Bring the application out of maintenance mode_

> **Tip:** Re-enable public access once maintenance is complete.
 
---
```bash
achievements:load
```
_Load all Achievements to database_

> **Note:** Updates achievement data. Run this after modifying achievement configurations.
 
---
```bash
auth:clear-resets
```
_Flush expired password reset tokens_

> **Tip:** Keeps your password reset table clean and secure.
 
---
```bash
auto:ban_disposable_users
```
_Ban user if using a disposable email_

> **Note:** Prevents signups with temporary emails. Enhances user quality.
 
---
```bash
auto:bon_allocation
```
_Allocates bonus points to users based on peer activity_

> **Tip:** Incentivizes active participation by awarding bonus points.
 
---
```bash
auto:cache_random_media
```
_Caches valid media IDs for random media component_

> **Note:** Improves performance for features displaying random media.
 
---
```bash
auto:cache_user_leech_counts
```
_Caches user leech counts_

> **Tip:** Speeds up retrieval of user statistics. Run this if leech counts appear slow.
 
---
```bash
auto:correct_history
```
_Corrects history records that appear active despite not receiving a STOPPED event from the client_

> **Note:** Fixes inconsistencies in history logs. Useful after client update issues.
 
---
```bash
auto:deactivate_warning
```
_Automatically deactivates user warnings if expired_

> **Tip:** Ensures warnings are only active while relevant.
 
---
```bash
auto:delete_stopped_peers
```
_Deletes all stopped peers_

> **Note:** Cleans up outdated peer data. Run this regularly to maintain accurate stats.
 
---
```bash
auto:delete_unparticipated_conversations
```
_Deletes conversations where all users have deleted their participation_

> **Tip:** Helps manage database size by removing obsolete conversation threads.
 
---
```bash
auto:disable_inactive_users
```
_Disables inactive user accounts based on criteria_

> **Note:** Automatically deactivates users who have been inactive, improving system efficiency.
 
---
```bash
auto:email-blacklist-update
```
_Updates the cache for email domains blacklist_

> **Tip:** Keeps the email blacklist current to prevent spam registrations.
 
---
```bash
auto:flush_peers
```
_Flushes ghost peers_

> **Note:** Clears inactive peer records, ensuring accurate connection counts.
 
---
```bash
auto:group
```
_Automatically changes a user’s group class if requirements are met_

> **Tip:** Dynamically updates user groups based on activity or role changes.
 
---
```bash
auto:highspeed_tag
```
_Updates torrents’ highspeed tag based on registered seedboxes_

> **Note:** Keeps torrent tagging up-to-date for performance and filtering.
 
---
```bash
auto:nerdstat
```
_Automatically posts daily nerd stats to the shoutbox_

> **Tip:** Engages users by displaying daily statistics. Run as a scheduled task.
 
---
```bash
auto:prewarning
```
_Automatically sends pre-warning notifications to users_

> **Note:** Alerts users before potential issues arise. Useful for proactive communication.
 
---
```bash
auto:recycle_audits
```
_Recycles audits once they are X days old_

> **Tip:** Archives old audit records, keeping your audit log manageable.
 
---
```bash
auto:recycle_claimed_torrent_requests
```
_Recycles torrent requests that were claimed but not filled within 7 days_

> **Note:** Frees up stalled torrent requests for new submissions.
 
---
```bash
auto:recycle_failed_logins
```
_Recycles failed logins once 30 days old_

> **Tip:** Clears out old failed login attempts to reduce database clutter.
 
---
```bash
auto:recycle_invites
```
_Recycles expired invites_

> **Note:** Reclaims unused invites, ensuring your invite system remains efficient.
 
---
```bash
auto:refund_download
```
_Refunds download credits to users based on seed time_

> **Tip:** Automates refunds for insufficient seeding, maintaining fairness.
 
---
```bash
auto:remove_expired_donors
```
_Automatically removes expired donors_

> **Note:** Cleans up donor statuses after their validity period ends.
 
---
```bash
auto:remove_featured_torrent
```
_Automatically removes featured torrents if expired_

> **Tip:** Keeps the featured torrents list current by removing outdated entries.
 
---
```bash
auto:remove_personal_freeleech
```
_Automatically removes a user’s personal freeleech if it has expired_

> **Note:** Ensures freeleech privileges are only active for their designated period.
 
---
```bash
auto:remove_torrent_buffs
```
_Automatically removes torrent buffs if expired_

> **Tip:** Manages temporary boosts on torrents, removing them when no longer valid.
 
---
```bash
auto:reset_user_flushes
```
_Resets the daily limit for users to flush their own peers_

> **Note:** Resets limits daily to maintain fair usage of the peer flushing feature.
 
---
```bash
auto:reward_resurrection
```
_Automatically hands out rewards for successful resurrections_

> **Tip:** Incentivizes users to revive stalled processes by offering rewards.
 
---
```bash
auto:softdelete_disabled_users
```
_Disables users in a disabled group for a specified period_

> **Note:** Temporarily soft-deletes users who meet the disabled criteria, enhancing system security.
 
---
```bash
auto:sync_peers
```
_Syncs torrent seeders, leechers, and times completed count_

> **Tip:** Ensures your torrent statistics remain accurate by synchronizing peer data.
 
---
```bash
auto:sync_people_to_meilisearch
```
_Syncs people to Meilisearch_

> **Note:** Updates the search index with the latest user data, ensuring search accuracy.
 
---
```bash
auto:sync_torrent_season_episode
```
_Syncs season and episode numbers from torrent titles to the database_

> **Tip:** Extracts and updates season/episode metadata automatically. Very useful for TV show torrents.
 
---
```bash
auto:sync_torrents_to_meilisearch
```
_Syncs torrents and their relations to Meilisearch_

> **Note:** Keeps the search index current with all torrent-related data. Run after major torrent updates.
 
---
```bash
auto:torrent_balance
```
_Calculates balance for all torrents_

> **Tip:** Recomputes torrent statistics to ensure fairness in credit allocation.
 
---
```bash
auto:update_user_last_actions
```
_Updates user last actions in batches_

> **Note:** Refreshes activity logs in bulk, useful for performance tuning during high load.
 
---
```bash
auto:upsert_announces
```
_Upserts announces in batches_

> **Tip:** Efficiently updates announcement data. Use when bulk changes are needed.
 
---
```bash
auto:upsert_histories
```
_Upserts peer histories in batches_

> **Note:** Batches updates to peer history records to minimize performance overhead.
 
---
```bash
auto:upsert_peers
```
_Upserts peers in batches_

> **Tip:** Refreshes peer records in bulk for accuracy and efficiency.
 
---
```bash
auto:warning
```
_Automatically posts warnings to users’ accounts and warnings table_

> **Note:** Sends automated warnings based on system triggers. Monitor warnings for any false positives.
 
---
```bash
backup:clean
```
_Removes all backups older than the specified number of days_

> **Tip:** Regularly run this command to free up storage and remove outdated backups.
 
---
```bash
backup:list
```
_Displays a list of all backups_

> **Note:** Quickly check available backups before performing restores or cleanups.
 
---
```bash
backup:monitor
```
_Monitors the health of all backups_

> **Tip:** Use this command to verify backup integrity and ensure your system’s data is secure.
 
---
```bash
backup:run
```
_Runs the backup process_

> **Note:** Initiates a new backup of your application. Always run this before major changes or deployments.
 
---
```bash
cache:clear
```
_Flushes the application cache_

> **Tip:** Use after configuration changes to ensure that the latest settings are applied.
 
---
```bash
cache:forget
```
_Removes an item from the cache_

> **Note:** Targets a specific cache key for removal. Useful for debugging caching issues.
 
---
```bash
cache:prune-stale-tags
```
_Prunes stale cache tags from the cache (Redis only)_

> **Tip:** Clean up outdated cache tags to improve cache performance in Redis environments.
 
---
```bash
channel:list
```
_Lists all registered private broadcast channels_

> **Note:** Helps verify that your broadcasting channels are correctly registered.
 
---
```bash
clean:torrent_files
```
_Cleans torrent files to remove extra unneeded data_

> **Tip:** Use this command to optimize disk space and remove redundant torrent data.
 
---
```bash
clear:all_cache
```
_Clears several common caches_

> **Note:** A broader cache clear command that resets multiple caches at once.
 
---
```bash
config:cache
```
_Creates a cache file for faster configuration loading_

> **Tip:** Run this command after modifying configuration files to speed up loading times.
 
---
```bash
config:clear
```
_Removes the configuration cache file_

> **Note:** Useful for debugging configuration issues when recent changes are not reflected.
 
---
```bash
config:publish
```
_Publishes configuration files to your application_

> **Tip:** Allows you to customize package configurations by copying them into your project.
 
---
```bash
config:show
```
_Displays all values for a given configuration file or key_

> **Note:** Use this command to inspect current configuration values for troubleshooting.
 
---
```bash
db:monitor
```
_Monitors the number of connections on the specified database_

> **Tip:** Provides insights into database connection load. Helpful for performance monitoring.
 
---
```bash
db:seed
```
_Seeds the database with records_

> **Note:** Populates your database with initial or test data. Run after migrations to populate tables.
 
---
```bash
db:show
```
_Displays information about the given database_

> **Tip:** Useful for a quick overview of database details and settings.
 
---
```bash
db:table
```
_Displays information about the given database table_

> **Note:** Shows the structure and data of a specific table. Great for debugging schema issues.
 
---
```bash
db:wipe
```
_Drops all tables, views, and types_

> **Tip:** A destructive command used mainly in development for resetting the database.
 
---
```bash
debugbar:clear
```
_Clears the Debugbar storage_

> **Note:** Clears stored debug information. Useful when debugging and needing fresh data.
 
---
```bash
demo:seed
```
_Seeds fake data for demonstration or testing purposes_

> **Tip:** Quickly populate your application with dummy data for demos or tests.
 
---
```bash
env:decrypt
```
_Decrypts an environment file_

> **Note:** Use this command to convert an encrypted environment file back to plaintext.
 
---
```bash
env:encrypt
```
_Encrypts an environment file_

> **Tip:** Secures sensitive environment data by encrypting it. Run this before deploying sensitive configurations.
 
---
```bash
event:cache
```
_Discovers and caches the application's events and listeners_

> **Note:** Improves performance by caching event listeners. Run this after modifying event files.
 
---
```bash
event:clear
```
_Clears all cached events and listeners_

> **Tip:** Use when changes in events or listeners aren’t reflecting; clears the event cache.
 
---
```bash
event:list
```
_Lists the application's events and listeners_

> **Note:** Provides a quick reference of registered events. Useful for debugging event-related issues.
 
---
```bash
fetch:meta
```
_Fetches meta data for new systems on preexisting torrents_

> **Tip:** Updates metadata for torrents. Run this when adding new system features that affect torrent data.
 
---
```bash
git:update
```
_Executes commands necessary to update your website using Git_

> **Note:** Automates parts of the deployment process by updating your code repository.
 
---
```bash
igdb:publish
```
_Publishes IGDB-Laravel configuration_

> **Tip:** Copies IGDB configuration files to your application for further customization.
 
---
```bash
igdb:webhooks
```
_Lists all your registered webhooks at IGDB_

> **Note:** Use to verify that your webhooks are correctly registered with IGDB.
 
---
```bash
igdb:webhooks:create
```
_Creates a webhook at IGDB_

> **Tip:** Sets up a new webhook for IGDB notifications. Ensure your IGDB credentials are configured.
 
---
```bash
igdb:webhooks:delete
```
_Deletes a webhook at IGDB_

> **Note:** Remove outdated or incorrect webhooks. Use with caution as this action is irreversible.
 
---
```bash
igdb:webhooks:reactivate
```
_Reactivates an inactive webhook_

> **Tip:** Re-enables a webhook that has been disabled, ensuring continuous data synchronization.
 
---
```bash
install:api
```
_Creates an API routes file and installs Laravel Sanctum or Laravel Passport_

> **Note:** Sets up API authentication scaffolding. Use this when starting a new API project.
 
---
```bash
install:broadcasting
```
_Creates a broadcasting channel routes file_

> **Tip:** Generates necessary files for event broadcasting. Useful when implementing real-time features.
 
---
```bash
irc:message
```
_Sends a message to an IRC channel_

> **Note:** Facilitates communication with IRC channels for notifications or updates.
 
---
```bash
key:generate
```
_Sets the application key_

> **Tip:** Essential for security. Run this when setting up a new Laravel project to generate a unique key.
 
---
```bash
lang:publish
```
_Publishes all language files available for customization_

> **Note:** Copies package language files into your project for localization. Use when customizing translations.
 
---
```bash
livewire:attribute
```
_Creates a new Livewire attribute class_

> **Tip:** Use when building custom attribute classes for Livewire components.
 
---
```bash
livewire:configure-s3-upload-cleanup
```
_Configures S3 temporary file upload cleanup for files older than 24 hours_

> **Note:** Automates cleanup of old S3 uploads. Use this to maintain storage hygiene in S3 environments.
 
---
```bash
livewire:copy
```
_Copies a Livewire component_

> **Tip:** Duplicate an existing Livewire component as a starting point for new features.
 
---
```bash
livewire:delete
```
_Deletes a Livewire component_

> **Note:** Permanently removes a Livewire component from your project.
 
---
```bash
livewire:form
```
_Creates a new Livewire form class_

> **Tip:** Use to generate a form handler class for Livewire, speeding up form-related development.
 
---
```bash
livewire:layout
```
_Creates a new app layout file_

> **Note:** Sets up a new layout for Livewire components. Customize as needed for your application design.
 
---
```bash
livewire:make
```
_Creates a new Livewire component_

> **Tip:** Quickly scaffold a Livewire component with boilerplate code. Great for rapid prototyping.
 
---
```bash
livewire:move
```
_Moves a Livewire component_

> **Note:** Reorganizes component files. Useful during project restructuring.
 
---
```bash
livewire:publish
```
_Publishes Livewire configuration_

> **Tip:** Copies Livewire’s config file into your project, allowing for customization.
 
---
```bash
livewire:stubs
```
_Publishes Livewire stubs_

> **Note:** Provides customizable stub files for generating Livewire components.
 
---
```bash
livewire:upgrade
```
_Interactive upgrade helper to migrate from v2 to v3_

> **Tip:** Use this command when upgrading your Livewire version to ensure a smooth transition.
 
---
```bash
make:achievement
```
_Creates a new achievement class_

> **Note:** Scaffold a class for managing user achievements. Modify the generated file to suit your achievement logic.
 
---
```bash
make:achievement_chain
```
_Creates a new achievement chain class_

> **Tip:** Use for creating complex achievement sequences. Edit the generated class to define chain logic.
 
---
```bash
make:cache-table
```
_Creates a migration for the cache database table_

> **Note:** Generates a migration to build a dedicated cache table. Run migrations afterward.
 
---
```bash
make:cast
```
_Creates a new custom Eloquent cast class_

> **Tip:** Use to define custom casting logic for model attributes. Modify the generated class accordingly.
 
---
```bash
make:channel
```
_Creates a new channel class_

> **Note:** Generates a broadcast channel class for real-time communication. Customize as needed.
 
---
```bash
make:class
```
_Creates a new class_

> **Tip:** A generic command to scaffold a new PHP class. Use it when no other specific generator applies.
 
---
```bash
make:command
```
_Creates a new Artisan command_

> **Note:** Use this to create custom console commands. Customize the handle method with your command logic.
 
---
```bash
make:component
```
_Creates a new view component class_

> **Tip:** Scaffolds a component for use in your views. Customize the Blade template and class as required.
 
---
```bash
make:controller
```
_Creates a new controller class_

> **Note:** Generates a controller file. Use resource controllers for RESTful actions when possible.
 
---
```bash
make:enum
```
_Creates a new enum_

> **Tip:** Helps define a set of constant values. Use this for clean, type-safe enumerations.
 
---
```bash
make:event
```
_Creates a new event class_

> **Note:** Scaffolds an event class to be used with Laravel’s event broadcasting. Customize for your application needs.
 
---
```bash
make:exception
```
_Creates a new custom exception class_

> **Tip:** Use to create exceptions that can be caught and handled uniquely within your application.
 
---
```bash
make:factory
```
_Creates a new model factory_

> **Note:** Generates a factory for seeding your database. Modify it to produce realistic test data.
 
---
```bash
make:interface
```
_Creates a new interface_

> **Tip:** Define contracts for classes. Use interfaces to enforce method implementation consistency.
 
---
```bash
make:job
```
_Creates a new job class_

> **Note:** Scaffold a job for queued tasks. Customize the handle method for asynchronous processing.
 
---
```bash
make:job-middleware
```
_Creates a new job middleware class_

> **Tip:** Use to add middleware logic to queued jobs. Ideal for tasks that require pre- or post-processing.
 
---
```bash
make:listener
```
_Creates a new event listener class_

> **Note:** Automatically generates a listener for an event. Modify the handle method to perform actions upon event firing.
 
---
```bash
make:livewire
```
_Creates a new Livewire component_

> **Tip:** Speeds up the creation of interactive UI components with Livewire. Customize the generated files for your use case.
 
---
```bash
make:mail
```
_Creates a new email class_

> **Note:** Generates a mailable class for building email templates. Edit the build method to configure email content.
 
---
```bash
make:middleware
```
_Creates a new HTTP middleware class_

> **Tip:** Scaffold middleware to handle request filtering. Implement your logic in the handle method.
 
---
```bash
make:migration
```
_Creates a new migration file_

> **Note:** Use to generate migration files for database schema changes. Edit the file to define your table structure.
 
---
```bash
make:model
```
_Creates a new Eloquent model class_

> **Tip:** Scaffolds a model file. Customize attributes and relationships to match your database design.
 
---
```bash
make:notification
```
_Creates a new notification class_

> **Note:** Generates a notification class for sending alerts to users. Customize via mail, database, or other channels.
 
---
```bash
make:notifications-table
```
_Creates a migration for the notifications table_

> **Tip:** Prepares a migration to store notification data. Run migrations after creation.
 
---
```bash
make:observer
```
_Creates a new observer class_

> **Note:** Use to watch model events and trigger actions automatically. Edit methods to handle specific events.
 
---
```bash
make:policy
```
_Creates a new policy class_

> **Tip:** Generates a policy for authorization. Customize methods to restrict actions on models.
 
---
```bash
make:provider
```
_Creates a new service provider class_

> **Note:** Scaffold a provider to register services and bindings. Register it in the config if necessary.
 
---
```bash
make:queue-batches-table
```
_Creates a migration for the batches database table_

> **Tip:** Prepares a table for tracking queued job batches. Run migrations after generating.
 
---
```bash
make:queue-failed-table
```
_Creates a migration for the failed queue jobs database table_

> **Note:** Sets up a table to log failed jobs. Essential for debugging and retrying failed tasks.
 
---
```bash
make:queue-table
```
_Creates a migration for the queue jobs database table_

> **Tip:** Creates a table to store queued jobs. Use this when implementing queue functionality.
 
---
```bash
make:request
```
_Creates a new form request class_

> **Note:** Scaffold a request class for handling form validation. Customize the rules method to specify validations.
 
---
```bash
make:resource
```
_Creates a new resource_

> **Tip:** Generates a resource class for API responses. Use it to transform model data cleanly.
 
---
```bash
make:rule
```
_Creates a new validation rule_

> **Note:** Scaffold a custom validation rule. Edit the passes method to define your logic.
 
---
```bash
make:scope
```
_Creates a new scope class_

> **Tip:** Generates a query scope for models. Useful for reusable query constraints.
 
---
```bash
make:seeder
```
_Creates a new seeder class_

> **Note:** Scaffold a seeder to populate your database. Customize the run method with seed data.
 
---
```bash
make:session-table
```
_Creates a migration for the session database table_

> **Tip:** Sets up a table for session storage. Run migrations to implement session handling.
 
---
```bash
make:test
```
_Creates a new test class_

> **Note:** Generates a test file for your application. Write unit or feature tests in the generated file.
 
---
```bash
make:trait
```
_Creates a new trait_

> **Tip:** Use to create reusable code blocks. Traits help share common methods between classes.
 
---
```bash
make:view
```
_Creates a new view_

> **Note:** Scaffold a Blade view file. Customize it to design the frontend of your application.
 
---
```bash
migrate:fresh
```
_Drops all tables and re-runs all migrations_

> **Tip:** Useful for a complete database reset in development. Be cautious as it deletes all data.
 
---
```bash
migrate:install
```
_Creates the migration repository_

> **Note:** Sets up the necessary table to track migrations. Run this only once when setting up the project.
 
---
```bash
migrate:refresh
```
_Resets and re-runs all migrations_

> **Tip:** Combines rollback and migrate commands. Useful for refreshing your database schema.
 
---
```bash
migrate:reset
```
_Rolls back all database migrations_

> **Note:** Rolls back every migration. Use with caution, as it will remove all schema changes.
 
---
```bash
migrate:rollback
```
_Rolls back the last database migration_

> **Tip:** Use this to undo the most recent migration batch. Great for quick fixes during development.
 
---
```bash
migrate:status
```
_Shows the status of each migration_

> **Note:** Provides a summary of which migrations have been run. Use it to verify your migration history.
 
---
```bash
model:prune
```
_Prunes models that are no longer needed_

> **Tip:** Cleans up obsolete model records. Useful for maintaining database hygiene.
 
---
```bash
model:show
```
_Shows information about an Eloquent model_

> **Note:** Displays details of a model’s relationships and attributes. Useful for debugging model configurations.
 
---
```bash
octane:install
```
_Installs the Octane components and resources_

> **Tip:** Sets up Laravel Octane for improved performance. Run this during initial Octane configuration.
 
---
```bash
octane:reload
```
_Reloads the Octane workers_

> **Note:** Refreshes the Octane workers without full restart. Use when deploying updates.
 
---
```bash
octane:start
```
_Starts the Octane server_

> **Tip:** Boots the Octane server for high-performance PHP applications. Ideal for production environments.
 
---
```bash
octane:status
```
_Gets the current status of the Octane server_

> **Note:** Check this command to ensure Octane is running smoothly.
 
---
```bash
octane:stop
```
_Stops the Octane server_

> **Tip:** Gracefully shuts down the Octane server. Use during deployments or maintenance.
 
---
```bash
optimize:clear
```
_Removes the cached bootstrap files_

> **Note:** Clears all optimization caches. Useful when changes aren’t reflected after updates.
 
---
```bash
package:discover
```
_Rebuilds the cached package manifest_

> **Tip:** Automatically scans and caches package information. Run this after adding new packages.
 
---
```bash
pest:dataset
```
_Creates a new dataset file_

> **Note:** Generates a file for organizing test datasets. Useful for maintaining comprehensive tests.
 
---
```bash
pest:test
```
_Creates a new test file_

> **Tip:** Scaffold a new test file using Pest. Great for adopting a simplified testing framework.
 
---
```bash
queue:clear
```
_Deletes all jobs from the specified queue_

> **Note:** Clears queued jobs. Use with caution, as this will remove pending tasks.
 
---
```bash
queue:failed
```
_Lists all failed queue jobs_

> **Tip:** Check failed jobs to diagnose issues with background processing.
 
---
```bash
queue:flush
```
_Flushes all failed queue jobs_

> **Note:** Permanently removes all failed jobs. Useful when cleaning up after resolving issues.
 
---
```bash
queue:forget
```
_Deletes a failed queue job_

> **Tip:** Remove a specific failed job by its ID. Use this to manage individual job failures.
 
---
```bash
queue:listen
```
_Listens to a given queue_

> **Note:** Starts a listener that will process jobs as they arrive. Ideal for real-time job processing.
 
---
```bash
queue:monitor
```
_Monitors the size of the specified queues_

> **Tip:** Use this command to track queue length and performance, which can help in scaling worker processes.
 
---
```bash
queue:prune-batches
```
_Prunes stale entries from the batches database_

> **Note:** Cleans up old batch records from the queue system. Helps in maintaining performance.
 
---
```bash
queue:prune-failed
```
_Prunes stale entries from the failed jobs table_

> **Tip:** Removes outdated records from the failed jobs table to free up space.
 
---
```bash
queue:restart
```
_Restarts queue worker daemons after their current job_

> **Note:** Useful when deploying new code; it restarts workers to load updated configurations.
 
---
```bash
queue:retry
```
_Retries a failed queue job_

> **Tip:** Attempts to reprocess a failed job. Use this after addressing the underlying error.
 
---
```bash
queue:retry-batch
```
_Retries the failed jobs for a batch_

> **Note:** Useful for reprocessing a group of failed jobs collectively.
 
---
```bash
queue:work
```
_Starts processing jobs on the queue as a daemon_

> **Tip:** Launch a long-running worker to handle queued jobs continuously. Essential for production environments.
 
---
```bash
route:cache
```
_Creates a route cache file for faster route registration_

> **Note:** Speeds up route loading by caching routes. Run this before deploying to production.
 
---
```bash
route:clear
```
_Removes the route cache file_

> **Tip:** Use when route changes are not reflecting; clears the cached routes.
 
---
```bash
route:list
```
_Lists all registered routes_

> **Note:** Provides an overview of all available routes. Great for debugging routing issues.
 
---
```bash
sail:add
```
_Adds a service to an existing Sail installation_

> **Tip:** Use this to integrate additional services into your Docker-based Sail environment.
 
---
```bash
sail:install
```
_Installs Laravel Sail’s default Docker Compose file_

> **Note:** Sets up Sail for local development. Ideal for quickly configuring a Docker environment.
 
---
```bash
sail:publish
```
_Publishes the Laravel Sail Docker files_

> **Tip:** Copies Sail configuration files into your project for customization.
 
---
```bash
sail-ssl:install
```
_Installs the Nginx container in Docker Compose_

> **Note:** Sets up an Nginx container with SSL support. Use this for secure local development.
 
---
```bash
sail-ssl:publish
```
_Publishes the Nginx resources_

> **Tip:** Exports Nginx configuration files for customization. Useful for fine-tuning SSL settings.
 
---
```bash
schedule:clear-cache
```
_Deletes the cached mutex files created by the scheduler_

> **Note:** Clears cached scheduler locks. Run this if scheduled tasks aren’t executing as expected.
 
---
```bash
schedule:interrupt
```
_Interrupts the current schedule run_

> **Tip:** Stops the current scheduled command execution. Use this when you need to halt a long-running schedule.
 
---
```bash
schedule:list
```
_Lists all scheduled tasks_

> **Note:** Provides a summary of all tasks scheduled via the scheduler. Great for verifying cron setups.
 
---
```bash
schedule:run
```
_Runs the scheduled commands_

> **Tip:** Manually triggers all scheduled tasks. Useful for testing your scheduler outside of cron.
 
---
```bash
schedule:test
```
_Runs a scheduled command_

> **Note:** Executes a single scheduled task for testing purposes.
 
---
```bash
schedule:work
```
_Starts the schedule worker_

> **Tip:** Runs scheduled tasks continuously. Ideal for development environments where real-time scheduling is required.
 
---
```bash
schema:dump
```
_Dumps the given database schema_

> **Note:** Exports your database schema into a file. Use for backup or versioning of your schema.
 
---
```bash
scout:delete-all-indexes
```
_Deletes all indexes_

> **Tip:** Use this to completely clear your search indexes. Run with caution.
 
---
```bash
scout:delete-index
```
_Deletes an index_

> **Note:** Removes a specific search index. Useful when re-indexing a model.
 
---
```bash
scout:flush
```
_Flushes all of the model's records from the index_

> **Tip:** Clears the search index for a model before a full re-import. Helps prevent duplicate entries.
 
---
```bash
scout:import
```
_Imports the given model into the search index_

> **Note:** Populates your search index with model data. Run after updating your database.
 
---
```bash
scout:index
```
_Creates an index_

> **Tip:** Establishes a new index for your search engine. Verify search engine configuration before using.
 
---
```bash
scout:sync-index-settings
```
_Syncs your configured index settings with your search engine (Meilisearch)_

> **Note:** Ensures that your search index settings match your configuration. Run this when modifying index options.
 
---
```bash
set:all_cache
```
_Sets several common caches_

> **Tip:** Rebuilds essential caches after clearing them. Use this command to restore optimal performance.
 
---
```bash
storage:link
```
_Creates the symbolic links configured for the application_

> **Note:** Establishes the required symlinks for storage access. Run this after installing your application.
 
---
```bash
storage:unlink
```
_Deletes existing symbolic links configured for the application_

> **Tip:** Removes broken or outdated symbolic links. Useful when reorganizing storage directories.
 
---
```bash
stub:publish
```
_Publishes all stubs available for customization_

> **Note:** Copies all stub files into your project for modification. Use this when you need custom scaffolding.
 
---
```bash
test:email
```
_Sends a test email to the owner account using the current mail configuration_

> **Tip:** Verify your mail configuration by sending a test email. Essential for ensuring your mail setup is working.
 
---
```bash
tickets:stale
```
_Checks for tickets open longer than 3 days_

> **Note:** Identifies support tickets that have not been addressed promptly. Use this to trigger follow-up actions.
 
---
```bash
vendor:publish
```
_Publishes any publishable assets from vendor packages_

> **Tip:** Copies vendor assets to your project. Use this after installing a new package that requires asset publishing.
 
---
```bash
view:cache
```
_Compiles all of the application's Blade templates_

> **Note:** Improves view performance by caching compiled templates. Run this before deploying to production.
 
---
```bash
view:clear
```
_Clears all compiled view files_

> **Tip:** Use this when view changes aren’t reflected, ensuring that outdated compiled views are removed.
