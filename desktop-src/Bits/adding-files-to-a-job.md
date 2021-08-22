---
title: Agregar archivos a un trabajo
description: Un trabajo contiene uno o varios archivos que desea transferir.
ms.assetid: fb6e7219-b6ca-4f72-b7a3-60d65e8f3892
keywords:
- bits de trabajo de transferencia, agregar archivos
- BITS de transferencia de archivos, agregar
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: b6c369c0a9ee207790d0370da6543c642ee294b072e0d91f1837cd734a6a625d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529275"
---
# <a name="adding-files-to-a-job"></a>Agregar archivos a un trabajo

Un trabajo contiene uno o varios archivos que desea transferir. Use uno de los métodos siguientes para agregar archivos a un trabajo:

<dl> <dt>

<span id="IBackgroundCopyJob__AddFile"></span><span id="ibackgroundcopyjob__addfile"></span><span id="IBACKGROUNDCOPYJOB__ADDFILE"></span>[**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
</dt> <dd>

Agrega un único archivo a un trabajo.

</dd> <dt>

<span id="IBackgroundCopyJob__AddFileSet"></span><span id="ibackgroundcopyjob__addfileset"></span><span id="IBACKGROUNDCOPYJOB__ADDFILESET"></span>[**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
</dt> <dd>

Agrega uno o varios archivos a un trabajo. Si va a agregar varios archivos, es más eficaz llamar a este método que llamar al **método AddFile** en un bucle.

</dd> <dt>

<span id="IBackgroundCopyJob3__AddFileWithRanges"></span><span id="ibackgroundcopyjob3__addfilewithranges"></span><span id="IBACKGROUNDCOPYJOB3__ADDFILEWITHRANGES"></span>[**IBackgroundCopyJob3::AddFileWithRanges**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges)
</dt> <dd>

Agrega un único archivo a un trabajo. Use este método si desea descargar intervalos de datos de un archivo. Este método solo se puede usar para los trabajos de descarga.

</dd> </dl>

Al agregar un archivo a un trabajo, se especifica el nombre remoto y el nombre local del archivo. Para más información sobre el formato de los nombres de archivo locales y remotos, consulte la [**estructura BG \_ FILE \_ INFO.**](/windows/desktop/api/Bits/ns-bits-bg_file_info)

Un trabajo de carga solo puede contener un archivo. Los [**métodos IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile) e [**IBackgroundCopyJob::AddFileSet**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset) devuelven BG E TOO MANY FILES si intenta agregar más de un archivo a un trabajo de \_ \_ \_ \_ carga. Si necesita cargar más de un archivo, considere la posibilidad de usar un archivo CAB o ZIP.

Para los trabajos de descarga, BITS limita el número de archivos que un usuario puede agregar a un trabajo a 200 archivos y el número de intervalos de un archivo a 500 intervalos. Estos límites no se aplican a los administradores o servicios. Para cambiar estos límites predeterminados, vea [Directivas de grupo.](group-policies.md)

El propietario del trabajo o un usuario con privilegios de administrador pueden agregar archivos al trabajo en cualquier momento antes de llamar al método [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o al método [**IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)

Si necesita cambiar el nombre remoto del archivo después de agregar el archivo al trabajo, puede llamar al método [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o al método [**IBackgroundCopyFile2::SetRemoteName.**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) Use el **método ReplaceRemotePrefix** para cambiar la parte del servidor del nombre remoto cuando el servidor no está disponible o para permitir que los usuarios móviles se conecten al servidor más cercano. Use el **método SetRemoteName para** cambiar el protocolo usado para transferir el archivo o para cambiar el nombre de archivo o la ruta de acceso.

BITS crea un archivo temporal en el directorio de destino y usa el archivo temporal para la transferencia de archivos. Para obtener el nombre de archivo temporal, llame [**al método IBackgroundCopyFile3::GetTemporaryName.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) BITS cambia el nombre de archivo temporal al nombre de archivo de destino cuando se llama al [**método**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Complete. BITS no especifica un descriptor de seguridad cuando [**crea el**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) archivo temporal (el archivo hereda la información de ACL del directorio de destino). Si los datos transferidos son confidenciales, la aplicación debe especificar una ACL adecuada en el directorio de destino para evitar el acceso no autorizado.

Para mantener la información del propietario y la ACL con el archivo transferido, llame al método [**IBackgroundCopyJob3::SetFileACLFlags.**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-setfileaclflags)

El propietario del trabajo (el usuario que creó el trabajo o el administrador que tomó posesión del trabajo) debe tener permisos para el archivo en el servidor, así como en el cliente. [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership) Por ejemplo, para descargar un archivo, el usuario debe tener permisos de lectura en el servidor y permisos de escritura en el directorio local en el cliente.

En el ejemplo siguiente se muestra cómo agregar un único archivo al trabajo. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, es válido.


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



En el ejemplo siguiente se muestra cómo agregar varios archivos al trabajo. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, es válido y que los nombres locales y remotos proceden de una lista de la interfaz de usuario.


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



 

 