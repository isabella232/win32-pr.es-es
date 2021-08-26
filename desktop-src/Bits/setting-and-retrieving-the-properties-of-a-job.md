---
title: Establecer y recuperar las propiedades de un trabajo
description: El propietario del trabajo o un usuario con privilegios de administrador pueden establecer y recuperar las propiedades del trabajo en cualquier momento.
ms.assetid: 5d0ab96b-b818-4b41-8317-cf50ad17c12d
keywords:
- bits de trabajo de transferencia, propiedades
- establecer bits de propiedades de trabajo
- recuperación de bits de propiedades de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ded532d3c99c8f8063a5c372c60086f35320d321860b056b60f2cb5a9a4003
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004835"
---
# <a name="setting-and-retrieving-the-properties-of-a-job"></a>Establecer y recuperar las propiedades de un trabajo

El propietario del trabajo o un usuario con privilegios de administrador pueden establecer y recuperar las propiedades del trabajo en cualquier momento. Para obtener una lista completa de las propiedades que puede establecer y recuperar, vea las interfaces [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2,**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)e [**IBackgroundCopyJob4.**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)

Los archivos también contienen propiedades. Para obtener información sobre cómo recuperar un archivo y sus propiedades de un trabajo, vea [Enumerar archivos en un trabajo.](enumerating-files-in-a-job.md)

Para transferir archivos, no es necesario cambiar los valores predeterminados de las propiedades del trabajo: BITS usa valores predeterminados que son adecuados para la aplicación típica.

## <a name="setting-the-properties-of-a-job"></a>Establecimiento de las propiedades de un trabajo

En el ejemplo siguiente se muestra cómo establecer las propiedades que es más probable que cambie la aplicación: [priority](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority), [notify interface](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface), [notify flags](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)y [reply file name](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename). En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, es válido.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob4* pJob4 = NULL;
CNotifyInterface *pNotify = new CNotifyInterface();

hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob4), (void**)&pJob4);
pJob->Release();

//The default priority level for a job is BG_JOB_PRIORITY_NORMAL. 
hr = pJob4->SetPriority(BG_JOB_PRIORITY_HIGH);
if (FAILED(hr))
{
  //Handle error
}

//By default, an application must poll BITS for the status of a job.
//To specify an IBackgroundCopyCallback interface pointer that receives event 
//notification based on the value of the notify flags property, set the notify 
//interface property. For details on the CNotifyInterface example class, see the 
//IBackgroundCopyCallback interface in the reference section.
hr = pJob4->SetNotifyInterface(pNotify);
if (SUCCEEDED(hr))
{
  hr = pJob4->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                            BG_NOTIFY_JOB_ERROR);
}
pNotify->Release();
if (FAILED(hr))
{
  //Handle error - failed to setup notification callbacks
}

//Only set the reply file name if the job's type is BG_JOB_TYPE_UPLOAD_REPLY.
//If you do not set the file name before calling the IBackgroundCopyJob::Resume 
//method, BITS generates a file name for you; the directory is the same as that
//specified for the local file name (the file being uploaded). To retrieve the 
//file name, call the IBackgroundCopyJob2::GetReplyFileName method.
hr = pJob4->SetReplyFileName(L"<REPLYPATHGOESHERE>");
if (FAILED(hr))
{
  //Handle error
}
pJob4->Release();
```



De forma predeterminada, BITS descarga contenido del servidor de origen. Para descargar contenido de un elemento del mismo nivel, tanto el equipo como el trabajo deben habilitar el almacenamiento en caché del mismo nivel. Para habilitar el almacenamiento en caché del mismo nivel en el equipo, establezca la configuración de directiva de grupo EnablePeerCaching. También puede llamar al método [**IBitsPeerCacheAdministration::SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) para habilitar el almacenamiento en caché del mismo nivel en el equipo; sin embargo, la configuración de preferencias se invalida mediante la directiva, si se establece. Para habilitar el almacenamiento en caché del mismo nivel para el trabajo, debe llamar al método [**IBackgroundCopyJob4::SetPeerCachingFlags.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags)

Para especificar encabezados personalizados, un certificado de cliente para la autenticación de cliente y opciones HTTP como la directiva de redireccionamiento, la comprobación de CRL y la especificación de los errores de certificado que se omitirán, use la interfaz [**IBackgroundCopyJobHttpOptions.**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) Para obtener la **interfaz IBackgroundCopyJobHttpOptions,** consulte cualquiera de las interfaces [**IBackgroundCopyJob.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)

## <a name="retrieving-the-properties-of-a-job"></a>Recuperación de las propiedades de un trabajo

En el ejemplo siguiente se muestra cómo recuperar los valores de propiedad de [nombre](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)para mostrar [,](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) [propietario,](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)progreso [y](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) estado de un trabajo. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, es válido.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR* pszJobName = NULL;
WCHAR* pszOwnerSid = NULL;
BOOL bResult;
DWORD dwNameSize = 0;
DWORD dwDomainSize = 0;
WCHAR* pszName = NULL;
WCHAR* pszDomain = NULL;
WCHAR* pszFullOwnerName = NULL;
PSID pSid = NULL;
SID_NAME_USE eNameUse;
BG_JOB_PROGRESS Progress;
int PercentOfFiles = 0;
BG_JOB_PRIORITY Priority;
BG_JOB_STATE State;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

//Name of the job to use in the user interface. The name is set when you 
//create the job. You can use the SetDisplayName method to change the name. 
hr = pJob->GetDisplayName(&pszJobName);
if (SUCCEEDED(hr))
{
  //Use the name in a user interface or output.
  CoTaskMemFree(pszJobName);       
}

//The owner property contains the SID of the job's owner. The following code
//shows how to get the domain and user names associated with the SID.
hr = pJob->GetOwner(&pszOwnerSID);
if (SUCCEEDED(hr))
{
  bResult = ConvertStringSidToSid(pszOwnerSid, &pSid);
  CoTaskMemFree(pszOwnerSid);
  if (bResult)
  {
    //Call LookupAccountSid twice. The first call retrieves the buffer size 
    //for name and domain and the second call retrieves the actual name and domain.
    LookupAccountSid(NULL, pSid, NULL, &cbNameSize, 
                               NULL, &cbDomainSize, &eNameUse);
    LastError = GetLastError();
    if (ERROR_INSUFFICIENT_BUFFER == LastError)
    {
      pszName = (WCHAR*)malloc(sizeof(WCHAR) * cbNameSize);
      pszDomain = (WCHAR*)malloc(sizeof(WCHAR) * cbDomainSize);
      if (pszName && pszDomain)
      {
        bResult = LookupAccountSid(NULL, pSid, pszName, &cbNameSize, 
                                   pszDomain, &cbDomainSize, &eNameUse);
        if (bResult)
        {
          pszFullName = (WCHAR*)malloc(sizeof(WCHAR)*(cbDomainSize+1+cbNameSize+1));
          if (pszFullName)
          {
            StringCchPrintf(pszFullName, cbDomainSize+1+cbNameSize+1, L"%s\\%s", pszDomain, pszName);
            //Do something with pszFullName. 
            free(pszFullName);
          }
        }
      }
      if (pszDomain)
        free(pszDomain);
      if(pszName)
        free(pszName);
    }
    else
    {
      //Handle error - most likely ERROR_NONE_MAPPED, could not find the SID.
    }
    LocalFree(pSid);
  }
}

//The state property identifies the current state of the job. For example, the 
//state of the job is BG_JOB_STATE_TRANSFERRING or BG_JOB_STATE_ERROR. 
hr = pJob->GetState(&State);
if (SUCCEEDED(hr))
{
  //Use JobStates[State] to set the text representation of the job's 
  //state in a user interface.
}

//Use the information contained in the BG_JOB_PROGRESS structure to determine the 
//overall progress of the job. The structure contains information on the number of 
//bytes and files transferred. 
hr = pJob->GetProgress(&Progress);
if (SUCCEEDED(hr))
{
  //Determine the progress of the job based on the number of files transferred.
  if (Progress.FilesTotal > 0)
  {
    PercentOfFiles = 100*Progress.FilesTransferred/Progress.FilesTotal
  }
  //For an example that shows determining the progress of the job based on the 
  //number of bytes transferred, see the topic Determing the Progress of a Job.
}
```



 

 




