---
title: Registro de una devolución de llamada COM
description: En lugar de sondear los cambios en el estado de un trabajo, puede registrarse para recibir una notificación cuando cambie el estado del trabajo.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- transfer job BITS , event notification
- registro para bits de notificación de eventos
- BITS de notificación de eventos
- BITS de notificación de eventos, devoluciones de llamada
- BITS de eventos de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753feb481a578c30322d18def07418c2dcb611d601fcb438b0e85e843697790b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680009"
---
# <a name="registering-a-com-callback"></a>Registro de una devolución de llamada COM

En lugar [de sondear](polling-for-the-status-of-the-job.md) los cambios en el estado de un trabajo, puede registrarse para recibir una notificación cuando cambie el estado del trabajo. Para recibir una notificación, debe implementar la [**interfaz IBackgroundCopyCallback2.**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) La interfaz contiene los métodos siguientes a los que llama BITS, en función del registro:

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**FileTransferred**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Para obtener un ejemplo que implementa la [**interfaz IBackgroundCopyCallback2,**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) vea el código de ejemplo en el tema de la interfaz [**IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)

La [**interfaz IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) proporciona una notificación cuando se transfiere un archivo. Normalmente, se usa este método para validar el archivo, de modo que el archivo esté disponible para que lo descarguen los usuarios del mismo nivel. De lo contrario, el archivo no está disponible para los pares hasta que se llama al [**método IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Para validar el archivo, llame al [**método IBackgroundCopyFile3::SetValidationState.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate)

Hay dos métodos para registrar una devolución de llamada COM: registrar un objeto de devolución de llamada o registrar un identificador de clase de devolución de llamada. El uso de un objeto de devolución de llamada es más sencillo y una sobrecarga menor. usar un CLSID de devolución de llamada es más confiable, pero más complicado. Puede registrar , ambos o ninguno: BITS usará un objeto de devolución de llamada si existe uno y todavía se puede llamar a , y volverá a crear instancias de un nuevo objeto basado en un identificador de clase proporcionado si se produce un error.

### <a name="registering-a-callback-object"></a>Registrar un objeto de devolución de llamada

Para registrar la implementación con BITS, llame al [**método IBackgroundCopyJob::SetNotifyInterface.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) Para especificar a qué métodos llama BITS, llame al [**método IBackgroundCopyJob::SetNotifyFlags.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)

La interfaz de notificación deja de ser válida cuando finaliza la aplicación; BITS no conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe registrar los trabajos existentes para los que desea recibir la notificación. Si necesita capturar información de estado y progreso que se produjo desde la última vez que se ha ejecutado la aplicación, sondee la información de estado y progreso durante la inicialización de la aplicación.

Antes de salir, la aplicación debe borrar el puntero de interfaz de devolución de llamada (**SetNotifyInterface(NULL)**). Es más eficaz borrar el puntero de devolución de llamada que permitir que BITS detecte que ya no es válido.

Tenga en cuenta que si más de una aplicación llama al método [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para establecer la interfaz de notificación para el trabajo, la última aplicación que llama al método **SetNotifyInterface** es la que recibirá notificaciones; las demás aplicaciones no recibirán notificaciones.

En el ejemplo siguiente se muestra cómo registrarse para recibir notificaciones. En el ejemplo se supone que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido. Para obtener más información sobre la clase de ejemplo CNotifyInterface que se usa en el ejemplo siguiente, vea la [**interfaz IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a>Registrar un CLSID de devolución de llamada

Para registrar un CLSID de devolución de llamada con BITS, llame al método [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) con el valor **de PROPERTY NOTIFICATION \_ \_ \_ \_ CLSID** propertyId de BITS JOB. Para especificar a qué métodos llama BITS, llame al [**método IBackgroundCopyJob::SetNotifyFlags.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)

Debe asegurarse de que el CLSID de notificación está registrado en un servidor COM fuera de proceso antes de registrar el CLSID con un trabajo de BITS. Implementar un servidor [COM es mucho](/windows/desktop/com/com-server-responsibilities) más complicado que definir y pasar un objeto de devolución de llamada, pero ofrece varias ventajas importantes. Un servidor COM permite a BITS mantener la asociación entre un trabajo de BITS y el código de la aplicación a través de reinicios del sistema y para trabajos grandes o de larga duración. Un servidor COM también permite que la aplicación se apague completamente mientras BITS sigue ejecutando transferencias en segundo plano, lo que puede mejorar el uso de la batería, la CPU y la memoria del sistema.

Para proporcionar una notificación que se ha registrado para recibir, BITS intenta primero llamar al método correspondiente de cualquier objeto de devolución de llamada existente que pueda haber asociado. Si no hay ningún objeto existente o si ese objeto existente se ha desconectado (normalmente como resultado de la finalización de la aplicación), BITS llamará a CoCreateInstance mediante la notificación CLSID para crear una instancia de un nuevo objeto de devolución de llamada y usará ese objeto para cualquier devolución de llamada adicional hasta que se desconecte o se reemplazó por una nueva llamada a [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).

A diferencia de los objetos de devolución de llamada, el CLSID de devolución de llamada se conserva junto con sus trabajos de BITS correspondientes si el servicio BITS o el sistema se apagan y reinician. La aplicación puede borrar cualquier CLSID de notificación previamente establecido antes de salir (o en cualquier otro momento) pasando un nuevo CLSID de notificación de GUID NULL, pero es posible que la aplicación prefiera dejar registrada la notificación CLSID si la aplicación se ha registrado para que COM lo inicie en respuesta a las solicitudes \_ de CoCreateInstance para el CLSID. Tenga en cuenta que si más de una aplicación establece las llamadas a la propiedad CLSID DE NOTIFICACIÓN DE PROPIEDAD DE BITS JOB, el último **\_ \_ \_ \_ CLSID** que se va a establecer es el que BITS usará para crear instancias de objetos de devolución de llamada; no se crearán instancias de los otros CLSID. Del mismo modo, si una aplicación registra un CLSID y otra registra un objeto de devolución de llamada, se aplican las reglas habituales para el objeto de devolución de llamada que tiene prioridad y no se usará el CLSID a menos que el objeto de devolución de llamada se borra o se desconecta.

En el ejemplo siguiente se muestra cómo registrarse para las notificaciones CLSID. En el ejemplo se supone que el puntero de interfaz [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) es válido y que la aplicación ya se ha registrado como un servidor COM fuera de proceso que implementa la clase CNotifyInterface. Para obtener más información sobre la clase de ejemplo CNotifyInterface que se usa en el ejemplo siguiente, vea la [**interfaz IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 