logs_dir=$1 # Path to the logs to archive
archive_name=$(date +"log_archive_%y%m%d_%H%M%S") # Archive name
log_store_dir=${2:-"./"} # Where logs are going to be stored

tar -czf ${log_store_dir}${archive_name}.tar.gz ${logs_dir}

echo "Finished! The logs are stored at ${log_store_dir}"
