---
title: Agregar archivos a un trabajo
description: Un trabajo contiene uno o varios archivos que desea transferir.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- transferir BITS de trabajo, agregar archivos
- BITS de transferencia de archivos, agregar
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: ecb46a535fee117750b8b46066d798a4525aa44c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995398"
---
# <a name="adding-files-to-a-job"></a><span data-ttu-id="f4fd2-105">Agregar archivos a un trabajo</span><span class="sxs-lookup"><span data-stu-id="f4fd2-105">Adding Files to a Job</span></span>

<span data-ttu-id="f4fd2-106">Un trabajo contiene uno o varios archivos que desea transferir.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-106">A job contains one or more files that you want to transfer.</span></span> <span data-ttu-id="f4fd2-107">Use uno de los métodos siguientes para agregar archivos a un trabajo:</span><span class="sxs-lookup"><span data-stu-id="f4fd2-107">Use one of the following methods to add files to a job:</span></span>

<dl> <dt>

<span data-ttu-id="f4fd2-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span><span class="sxs-lookup"><span data-stu-id="f4fd2-108"><span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)</span></span>
</dt> <dd>

<span data-ttu-id="f4fd2-109">Agrega un solo archivo a un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-109">Adds a single file to a job.</span></span>

</dd> <dt>

<span data-ttu-id="f4fd2-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span><span class="sxs-lookup"><span data-stu-id="f4fd2-110"><span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)</span></span>
</dt> <dd>

<span data-ttu-id="f4fd2-111">Agrega uno o varios archivos a un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-111">Adds one or more files to a job.</span></span> <span data-ttu-id="f4fd2-112">Si va a agregar varios archivos, es más eficaz llamar a este método que llamar al método **AddFile** en un bucle.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-112">If you are adding multiple files, it is more efficient to call this method than to call the **AddFile** method in a loop.</span></span>

</dd> <dt>

<span data-ttu-id="f4fd2-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span><span class="sxs-lookup"><span data-stu-id="f4fd2-113"><span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)</span></span>
</dt> <dd>

<span data-ttu-id="f4fd2-114">Agrega un solo archivo a un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-114">Adds a single file to a job.</span></span> <span data-ttu-id="f4fd2-115">Use este método si desea descargar rangos de datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-115">Use this method if you want to download ranges of data from a file.</span></span> <span data-ttu-id="f4fd2-116">Este método solo se puede usar para trabajos de descarga.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-116">You can use this method only for download jobs.</span></span>

</dd> </dl>

<span data-ttu-id="f4fd2-117">Cuando se agrega un archivo a un trabajo, se especifica el nombre remoto y el nombre local del archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-117">When you add a file to a job, you specify the remote name and the local name of the file.</span></span> <span data-ttu-id="f4fd2-118">Para obtener más información sobre el formato de los nombres de archivos locales y remotos, consulte la estructura de [**\_ \_ información del archivo BG**](/windows/desktop/api/Bits/ns-bits-bg_file_info) .</span><span class="sxs-lookup"><span data-stu-id="f4fd2-118">For details on the format of the local and remote file names, see the [**BG\_FILE\_INFO**](/windows/desktop/api/Bits/ns-bits-bg_file_info) structure.</span></span>

<span data-ttu-id="f4fd2-119">Un trabajo de carga solo puede contener un archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-119">An upload job can contain only one file.</span></span> <span data-ttu-id="f4fd2-120">Los métodos [**IBackgroundCopyJob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) y [**IBackgroundCopyJob:: AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) devuelven \_ \_ \_ un número de archivos BG e demasiados \_ si intenta agregar más de un archivo a un trabajo de carga.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-120">The [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) and [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) methods return BG\_E\_TOO\_MANY\_FILES if you try to add more than one file to an upload job.</span></span> <span data-ttu-id="f4fd2-121">Si necesita cargar más de un archivo, considere la posibilidad de usar un archivo. CAB o un archivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-121">If you need to upload more than one file, consider using a CAB or ZIP file.</span></span>

<span data-ttu-id="f4fd2-122">En el caso de los trabajos de descarga, BITS limita el número de archivos que puede Agregar un usuario a un trabajo a 200 archivos y el número de intervalos de un archivo a 500 intervalos.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-122">For download jobs, BITS limits the number of files that a user can add to a job to 200 files and the number of ranges for a file to 500 ranges.</span></span> <span data-ttu-id="f4fd2-123">Estos límites no se aplican a los administradores o servicios.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-123">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="f4fd2-124">Para cambiar estos límites predeterminados, consulte [directivas de grupo](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="f4fd2-124">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="f4fd2-125">El propietario del trabajo o un usuario con privilegios de administrador pueden agregar archivos al trabajo en cualquier momento antes de llamar al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o al método [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="f4fd2-125">The owner of the job or a user with administrator privileges can add files to the job anytime prior to calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>

<span data-ttu-id="f4fd2-126">Si necesita cambiar el nombre remoto del archivo después de agregar el archivo al trabajo, puede llamar al método [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o al método [**IBackgroundCopyFile2:: SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) .</span><span class="sxs-lookup"><span data-stu-id="f4fd2-126">If you need to change the remote name of the file after you add the file to the job, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) method or the [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method.</span></span> <span data-ttu-id="f4fd2-127">Use el método **ReplaceRemotePrefix** para cambiar la parte del servidor del nombre remoto cuando el servidor no está disponible o para permitir que los usuarios móviles se conecten al servidor más cercano.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-127">Use the **ReplaceRemotePrefix** method to change the server portion of the remote name when the server is unavailable or to let roaming users connect to the closest server.</span></span> <span data-ttu-id="f4fd2-128">Use el método **SetRemoteName** para cambiar el protocolo que se usa para transferir el archivo o para cambiar el nombre de archivo o la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-128">Use the **SetRemoteName** method to change the protocol used to transfer the file or to change the file name or path.</span></span>

<span data-ttu-id="f4fd2-129">BITS crea un archivo temporal en el directorio de destino y usa el archivo temporal para la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-129">BITS creates a temporary file in the destination directory and uses the temporary file for the file transfer.</span></span> <span data-ttu-id="f4fd2-130">Para obtener el nombre de archivo temporal, llame al método [**IBackgroundCopyFile3:: GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) .</span><span class="sxs-lookup"><span data-stu-id="f4fd2-130">To get the temporary file name, call the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method.</span></span> <span data-ttu-id="f4fd2-131">BITS cambia el nombre del archivo temporal por el nombre del archivo de destino cuando se llama al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="f4fd2-131">BITS changes the temporary file name to the destination file name when you call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="f4fd2-132">BITS no especifica un descriptor de seguridad al [**crear**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) el archivo temporal (el archivo hereda la información de la ACL del directorio de destino).</span><span class="sxs-lookup"><span data-stu-id="f4fd2-132">BITS does not specify a security descriptor when it [**creates**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) the temporary file (the file inherits the ACL information from the destination directory).</span></span> <span data-ttu-id="f4fd2-133">Si los datos transferidos son confidenciales, la aplicación debe especificar una ACL adecuada en el directorio de destino para evitar el acceso no autorizado.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-133">If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.</span></span>

<span data-ttu-id="f4fd2-134">Para mantener la información de propietario y ACL con el archivo transferido, llame al método [**IBackgroundCopyJob3:: SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) .</span><span class="sxs-lookup"><span data-stu-id="f4fd2-134">To maintain the owner and ACL information with the transferred file, call the [**IBackgroundCopyJob3::SetFileACLFlags**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags) method.</span></span>

<span data-ttu-id="f4fd2-135">El propietario del trabajo (el usuario que creó el trabajo o el administrador que [tomó posesión](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) del trabajo) debe tener permisos para el archivo en el servidor y en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-135">The owner of the job (the user who created the job or the administrator who [took ownership](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) of the job) must have permissions to the file on the server as well as the client.</span></span> <span data-ttu-id="f4fd2-136">Por ejemplo, para descargar un archivo, el usuario debe tener permisos de lectura en el servidor y permisos de escritura en el directorio local en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-136">For example, to download a file the user must have read permissions on the server and write permissions to the local directory on the client.</span></span>

<span data-ttu-id="f4fd2-137">En el ejemplo siguiente se muestra cómo agregar un solo archivo al trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-137">The following example shows how to add a single file to the job.</span></span> <span data-ttu-id="f4fd2-138">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, es válido.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-138">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;

//Replace parameters with variables that contain valid paths.
hr = pJob->AddFile(L"https://ServerName/Path/File.Ext", L"d:\\Path\\File.Ext");
if (SUCCEEDED(hr))
{
  //Do something.
}
```



<span data-ttu-id="f4fd2-139">En el ejemplo siguiente se muestra cómo agregar varios archivos al trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-139">The following example shows how to add multiple files to the job.</span></span> <span data-ttu-id="f4fd2-140">En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) , pJob, es válido y los nombres locales y remotos proceden de una lista de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f4fd2-140">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer, pJob, is valid and the local and remote names come from a list in the user interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
ULONG idx = 0;
ULONG nCount = 0;            //Set to the number of files to add to the job.
LPWSTR pszLocalName = NULL;  //Comes from the list in the user interface.
LPWSTR pszRemoteName = NULL; //Comes from the list in the user interface.

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```



 

 