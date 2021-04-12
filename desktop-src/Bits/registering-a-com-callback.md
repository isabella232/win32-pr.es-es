---
title: Registrar una devolución de llamada COM
description: En lugar de sondear los cambios en el estado de un trabajo, puede registrarse para recibir notificaciones cuando el estado del trabajo cambie.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- transferir BITS de trabajo, notificación de eventos
- registro para BITS de notificación de eventos
- BITS de notificación de eventos
- BITS de notificación de eventos, devoluciones de llamada
- BITS de eventos de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359160"
---
# <a name="registering-a-com-callback"></a>Registrar una devolución de llamada COM

En lugar de [sondear](polling-for-the-status-of-the-job.md) los cambios en el estado de un trabajo, puede registrarse para recibir notificaciones cuando el estado del trabajo cambie. Para recibir la notificación, debe implementar la interfaz [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) . La interfaz contiene los métodos siguientes que llama a BITS, en función del registro:

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**FileTransferred**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Para obtener un ejemplo que implementa la interfaz [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , vea el ejemplo de código en el tema de la interfaz [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .

La interfaz [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) proporciona una notificación cuando se transfiere un archivo. Normalmente, este método se usa para validar el archivo, de modo que el archivo esté disponible para que los elementos del mismo nivel lo descarguen. de lo contrario, el archivo no estará disponible para los elementos del mismo nivel hasta que se llame al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Para validar el archivo, llame al método [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .

Hay dos métodos para registrar una devolución de llamada COM: registrar un objeto de devolución de llamada o registrar un identificador de clase de devolución de llamada. El uso de un objeto de devolución de llamada es más sencillo y reduce la sobrecarga; el uso de un CLSID de devolución de llamada es más confiable, pero más complicado. Puede registrar, ambos o ninguno: BITS usará un objeto de devolución de llamada si existe y todavía se puede llamar a, y volverá a crear instancias de un nuevo objeto basándose en un identificador de clase proporcionado si se produce un error.

### <a name="registering-a-callback-object"></a>Registrar un objeto de devolución de llamada

Para registrar la implementación con BITS, llame al método [**IBackgroundCopyJob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) . Para especificar qué métodos llama a BITS, llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).

La interfaz de notificación deja de ser válida cuando finaliza la aplicación; BITS no conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe registrar los trabajos existentes para los que desea recibir la notificación. Si necesita capturar información sobre el estado y el progreso que se produjeron desde la última vez que se ejecutó la aplicación, sondee la información sobre el estado y el progreso durante la inicialización de la aplicación.

Antes de salir, la aplicación debe borrar el puntero de la interfaz de devolución de llamada (**SetNotifyInterface (NULL)**). Es más eficaz borrar el puntero de devolución de llamada que para permitir que los BITS detecten que ya no es válido.

Tenga en cuenta que si más de una aplicación llama al método [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para establecer la interfaz de notificación para el trabajo, la última aplicación que llama al método **SetNotifyInterface** es la que recibirá notificaciones; las demás aplicaciones no recibirán notificaciones.

En el ejemplo siguiente se muestra cómo registrar las notificaciones. En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido. Para obtener más información sobre la clase de ejemplo CNotifyInterface que se usa en el ejemplo siguiente, vea la interfaz [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


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

Para registrar un CLSID de devolución de llamada con BITS, llame al método [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) con el CLSID de notificación de la **\_ propiedad del trabajo de \_ \_ \_ bits** . Para especificar qué métodos llama a BITS, llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .

Debe asegurarse de que el CLSID de notificación está registrado en un servidor COM fuera de proceso antes de registrar el CLSID con un trabajo de BITS. La implementación de un [servidor com](/windows/desktop/com/com-server-responsibilities) es significativamente más complicada que definir y pasar un objeto de devolución de llamada, pero ofrece varias ventajas importantes. Un servidor COM permite que los BITS mantengan la asociación entre un trabajo de BITS y el código de la aplicación a través de reinicios del sistema, y para trabajos grandes o de larga duración. Un servidor COM también permite que la aplicación se cierre completamente mientras BITS sigue ejecutando transferencias en segundo plano, lo que puede mejorar el uso de la batería, la CPU y la memoria del sistema.

Para proporcionar una notificación que se ha registrado para recibir, BITS primero intenta llamar al método correspondiente de cualquier objeto de devolución de llamada existente que se haya adjuntado. Si no hay ningún objeto existente, o si ese objeto existente se ha desconectado (normalmente, como resultado de la finalización de la aplicación), BITS llamará a CoCreateInstance mediante el CLSID de notificación para crear una instancia de un nuevo objeto de devolución de llamada y usará ese objeto para todas las devoluciones de llamada posteriores hasta que se desconecte o se reemplace por una nueva llamada a [**IBackgroundCopyJob:**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)

A diferencia de los objetos de devolución de llamada, el CLSID de devolución de llamada se conserva junto con sus trabajos de BITS correspondientes si el servicio BITS o el sistema se cierran y se reinician. La aplicación puede borrar cualquier CLSID de notificación de conjunto anterior antes de salir (o en cualquier otro momento) pasando un nuevo CLSID de notificación de GUID \_ null, pero es posible que la aplicación prefiera dejar el CLSID de notificación registrado si la aplicación se ha registrado para que com lo inicie en respuesta a las solicitudes de CoCreateInstance para su CLSID. Tenga en cuenta que si más de una aplicación establece la **propiedad \_ \_ CLSID de \_ notificación \_** de la propiedad del trabajo de bits, el último CLSID que se establecerá es el que bits usará para crear instancias de los objetos de devolución de llamada; no se crearán instancias de los otros CLSID. Del mismo modo, si una aplicación registra un CLSID y otro registra un objeto de devolución de llamada, se aplican las reglas habituales para el objeto de devolución de llamada, y el CLSID no se utilizará a menos que el objeto de devolución de llamada se borre o se desconecte.

En el ejemplo siguiente se muestra cómo registrar las notificaciones CLSID. En el ejemplo se da por supuesto que el puntero de la interfaz [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) es válido y que la aplicación ya se ha registrado como un servidor com fuera de proceso que implementa la clase CNotifyInterface. Para obtener más información sobre la clase de ejemplo CNotifyInterface que se usa en el ejemplo siguiente, vea la interfaz [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


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



 

 