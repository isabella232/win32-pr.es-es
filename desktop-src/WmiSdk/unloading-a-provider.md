---
description: Una vez que WMI finaliza con un proveedor, descarga el proveedor de la memoria.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Descargar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123d8c4f6b9d9155cdc22dc435635466956bdb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544646"
---
# <a name="unloading-a-provider"></a>Descargar un proveedor

Una vez que WMI finaliza con un proveedor, descarga el proveedor de la memoria. La razón principal por la que WMI descarga un proveedor es conservar los recursos del sistema. Por lo tanto, debe agregar código que permita a WMI descargar el proveedor de una manera eficaz. Tarda desde el intervalo especificado en el control de caché hasta el doble de ese intervalo para que WMI Descargue un proveedor.

WMI descarga un proveedor de una de las siguientes maneras:

-   Descargar un proveedor una vez que el proveedor finaliza las tareas que se le han dado.
-   Descargue rápidamente todos los proveedores cuando el usuario apague el sistema. Tenga en cuenta que WMI descarga los proveedores en proceso cuando se cierra el servicio WMI desde la línea de comandos.

Aunque el primer escenario es más común, debe escribir el proveedor para ambas posibilidades.

En este tema se describen las siguientes secciones:

-   [Descargar un proveedor inactivo](#unloading-an-idle-provider)
-   [Obtener acceso al tiempo de inactividad de un proveedor](#accessing-the-idle-time-for-a-provider)
-   [Descargar un proveedor que también es un cliente WMI](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Descargar un proveedor durante el cierre](#unloading-a-provider-during-shutdown)
-   [Temas relacionados](#related-topics)

## <a name="unloading-an-idle-provider"></a>Descargar un proveedor inactivo

WMI realiza las siguientes acciones cuando descarga un proveedor inactivo:

-   Determina si el proveedor está inactivo.

    WMI utiliza la propiedad **ClearAfter** para determinar cuánto tiempo un proveedor puede permanecer inactivo antes de descargar ese proveedor. Para obtener más información, vea [obtener acceso al tiempo de inactividad de un proveedor](#accessing-the-idle-time-for-a-provider).

-   Llama al método de [**versión**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) del proveedor.

    Si el proveedor era un proveedor puro, [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quita completamente el proveedor de la memoria activa. Sin embargo, un proveedor no puro puede continuar ejecutándose después de que WMI llame a **Release**.

## <a name="accessing-the-idle-time-for-a-provider"></a>Obtener acceso al tiempo de inactividad de un proveedor

La cantidad mínima de tiempo que un proveedor permanece activo viene determinada por la propiedad **ClearAfter** . Puede encontrar **ClearAfter** en instancias de clases derivadas de la clase del sistema WMI [**\_ \_ CacheControl**](--cachecontrol.md) en el \\ espacio de nombres raíz.

En la lista siguiente se describen las clases que se derivan de [**\_ \_ CacheControl**](--cachecontrol.md), que controla la descarga del proveedor:

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

Puede cambiar la cantidad mínima de tiempo que WMI permite que un proveedor permanezca inactivo editando la propiedad **ClearAfter** en la instancia de control de caché para un tipo específico de proveedor. Por ejemplo, para limitar la cantidad de tiempo que un proveedor de propiedades puede permanecer inactivo, debe modificar la propiedad **ClearAfter** de una instancia de [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) en el \\ espacio de nombres raíz.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Descargar un proveedor que también es un cliente WMI

Es posible que el proveedor deba seguir siendo un cliente de WMI después de haber completado las funciones de proveedor a las que se llamó. Por ejemplo, un proveedor de inserciones puede necesitar emitir consultas a WMI. Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md). En este caso, la propiedad **pura** de la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor debe establecerse en **true**. Si la propiedad **Pure** está establecida en **false**, el proveedor se prepara para la descarga llamando a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al método de versión de su interfaz principal. Para obtener más información, vea la sección Comentarios en [**\_ \_ Win32Provider**](--win32provider.md).

En el procedimiento siguiente se describe cómo implementar un método de versión para la interfaz principal de su proveedor.

**Para descargar un proveedor**

1.  Libera todos los punteros de interfaz que se mantienen en WMI cuando WMI llama al método de [**versión**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de la interfaz principal de su proveedor.

    Normalmente, un proveedor contiene punteros a las interfaces [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) y [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) proporcionadas en [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).

2.  Si la propiedad **pura** de la instancia de [**\_ \_ Win32Provider**](--win32provider.md) asociada está establecida en **false**, el proveedor puede realizar la transición al rol de la aplicación cliente después de que WMI llame a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Sin embargo, WMI no puede descargar un proveedor que funciona como sistema cliente, lo que aumenta la sobrecarga del sistema.

    Un proveedor con **Pure** establecido en **true** solo existe para las solicitudes de servicio. Por lo tanto, este tipo de proveedor no puede asumir el rol de una aplicación cliente y WMI puede descargarlo.

## <a name="unloading-a-provider-during-shutdown"></a>Descargar un proveedor durante el cierre

En circunstancias normales, el uso de las instrucciones de [descarga de un proveedor que también es un cliente WMI](#unloading-a-provider-that-is-also-a-wmi-client) permite a WMI descargar el proveedor correctamente. Sin embargo, es posible que se ejecuten situaciones en las que WMI no pueda establecer los procedimientos de descarga normales, como cuando el usuario elige apagar el sistema. Mediante el uso de un modelo de transacción de almacenamiento de datos, además de implementar una buena estrategia de limpieza, puede asegurarse de que el proveedor se ha descargado correctamente.

El usuario puede detener WMI en cualquier momento. En tal situación, WMI no descarga ningún proveedor o llama al punto de entrada de [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) en cualquier proveedor en proceso. Además, si un proveedor en proceso está en medio de una llamada al método en el momento del cierre, WMI puede terminar el subproceso en medio de la llamada. En este caso, WMI no llama a rutinas que normalmente controlan la limpieza, como un destructor de objeto. Como máximo, WMI llamará solo a [**DllMain**](/windows/desktop/Dlls/dllmain) .

Cuando el sistema operativo apaga WMI, el sistema libera automáticamente toda la memoria asignada a un proveedor en proceso. El sistema operativo también cierra la mayoría de los recursos que mantiene el proveedor, como los identificadores de archivo, los identificadores de ventana, etc. No es necesario que el proveedor realice ninguna acción específica para que esto suceda.

Dado que WMI puede cerrarse en medio de una llamada, un proveedor no debe dejar los orígenes de datos en un estado incoherente. La salida de los datos en un estado incoherente no es un problema para los proveedores de solo lectura. Sin embargo, los proveedores con capacidades de escritura pueden querer implementar algún tipo de modelo de transacción para permitir una reversión segura después de una terminación brusca.

Aunque el sistema operativo puede liberar algunos recursos generales del sistema, el sistema no libera automáticamente todos los recursos. Por ejemplo, el sistema operativo puede no liberar un socket o una conexión de base de datos. En su lugar, es posible que el proveedor tenga que limpiar estos recursos manualmente. Para evitar estos problemas, puede implementar el proveedor fuera de proceso, o bien puede Agregar el código de limpieza.

La solución más sencilla consiste en implementar el proveedor fuera de proceso. Un proveedor fuera de proceso no se elimina cuando WMI se cierra, aunque WMI liberará al proveedor después de un tiempo de espera de COM. Los proveedores para los que los problemas de solidez de la limpieza y terminación son más importantes que el rendimiento puede estar fuera del proceso.

Si debe colocar el código de limpieza en el proveedor, tiene dos opciones. Un lugar para realizar este tipo de limpieza es [**DllMain**](/windows/desktop/Dlls/dllmain), la función de punto de entrada de dll a la que llama el sistema operativo al descargar el archivo dll. El código de limpieza se puede agregar directamente a **DllMain** y ejecutarlo en respuesta a la **\_ \_ desasociación del proceso dll**. Implementar el código de limpieza en **DllMain** puede ser algo difícil de organizar, especialmente en entornos de programación como MFC o ATL. Para obtener más información, vea el artículo de Microsoft Knowledge Base Q148791, "How to representate *Your Own in a MFC normal dll".* (Es posible que este recurso no esté disponible en algunos idiomas y países o regiones).

Como alternativa, también puede colocar el código de limpieza en el destructor de una clase global. Para obtener más información, vea descargar un proveedor. El sistema operativo Windows no asigna objetos globales en el montón. En su lugar, el sistema operativo llama a los destructores durante la descarga del archivo DLL.

A continuación se facilita un procedimiento de limpieza sencillo que podría caber dentro de un objeto global para WMI.


```C++
class CMyCleanup
{
    ~CMyCleanup()
    {
        CloseHandle(m_hOpenFile);
        CloseDatabaseConnection(g_hDatabase);
    }
} g_Cleanup;
```



Hay muchas restricciones en cuanto a lo que se puede hacer en el código de limpieza con cualquier enfoque. Por ejemplo, no se puede tener acceso a ninguno de los subprocesos ni a los archivos DLL que no estén vinculados de forma implícita. Además, no puede realizar llamadas COM en ningún caso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
