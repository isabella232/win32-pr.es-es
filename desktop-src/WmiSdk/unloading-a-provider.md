---
description: Una vez que WMI finaliza con un proveedor, descarga el proveedor de la memoria.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Descargar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b831f69ba27ab3e173920cc57e7500ef543bb327a04dc5c04dc8b0b9cef31ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049963"
---
# <a name="unloading-a-provider"></a>Descargar un proveedor

Una vez que WMI finaliza con un proveedor, descarga el proveedor de la memoria. La razón principal por la que WMI descarga un proveedor es para conservar los recursos del sistema. Por lo tanto, debe agregar código que permita a WMI descargar el proveedor de una manera eficaz. Se tarda desde el intervalo especificado en el control de caché hasta el doble de ese intervalo para que WMI descargue un proveedor.

WMI descarga un proveedor de una de las maneras siguientes:

-   Descargue un proveedor después de que el proveedor finalice las tareas que se le han dado.
-   Descargue rápidamente todos los proveedores cuando el usuario apague el sistema. Tenga en cuenta que WMI descarga los proveedores en proceso cuando el servicio WMI se cierra desde la línea de comandos.

Aunque el primer escenario es más común, debe escribir el proveedor para ambas posibilidades.

En este tema se de abordan las secciones siguientes:

-   [Descargar un proveedor inactivo](#unloading-an-idle-provider)
-   [Acceso al tiempo de inactividad de un proveedor](#accessing-the-idle-time-for-a-provider)
-   [Descargar un proveedor que también es un cliente WMI](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Descargar un proveedor durante el apagado](#unloading-a-provider-during-shutdown)
-   [Temas relacionados](#related-topics)

## <a name="unloading-an-idle-provider"></a>Descargar un proveedor inactivo

WMI realiza las siguientes acciones cuando descarga un proveedor inactivo:

-   Determina si el proveedor está inactivo.

    WMI usa la **propiedad ClearAfter** para determinar cuánto tiempo puede permanecer inactivo un proveedor antes de descargar ese proveedor. Para obtener más información, vea [Acceso al tiempo de inactividad de un proveedor.](#accessing-the-idle-time-for-a-provider)

-   Llama al [**método Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) del proveedor.

    Si el proveedor era un proveedor puro, [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quita completamente el proveedor de la memoria activa. Sin embargo, un proveedor nopure puede seguir en ejecución después de que WMI llame a **Release**.

## <a name="accessing-the-idle-time-for-a-provider"></a>Acceso al tiempo de inactividad de un proveedor

La cantidad mínima de tiempo que un proveedor permanece activo viene determinada por la **propiedad ClearAfter.** Puede encontrar **ClearAfter en instancias** de clases derivadas de la clase del sistema WMI [**\_ \_ CacheControl**](--cachecontrol.md) en el espacio de nombres \\ raíz.

En la lista siguiente se describen las clases derivadas de [**\_ \_ CacheControl**](--cachecontrol.md), que controla la descarga del proveedor:

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

Puede cambiar la cantidad mínima de tiempo que WMI permite que un proveedor permanezca inactivo editando la **propiedad ClearAfter** en la instancia de control de caché para un tipo específico de proveedor. Por ejemplo, para limitar la cantidad de tiempo que un proveedor de propiedades puede permanecer inactivo, debe editar la propiedad **ClearAfter** de una [**\_ \_ instancia de PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) en el espacio \\ de nombres raíz.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Descargar un proveedor que también es un cliente WMI

Es posible que el proveedor tenga que seguir siendo un cliente de WMI después de haber completado las funciones de proveedor a las que se llamó para realizar. Por ejemplo, un proveedor de inserción puede necesitar emitir consultas a WMI. Para obtener más información, vea [Determinar el estado de inserción o extracción.](determining-push-or-pull-status.md) En este caso, la **propiedad Pure** de la [**\_ \_ instancia de Win32Provider**](--win32provider.md) que representa el proveedor debe establecerse en **TRUE.** Si la **propiedad Pure** se establece en **FALSE,** el proveedor se prepara para descargar llamando a [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al método Release de su interfaz principal. Para obtener más información, vea la sección Comentarios de [**\_ \_ Win32Provider**](--win32provider.md).

En el procedimiento siguiente se describe cómo implementar un método de versión para la interfaz principal del proveedor.

**Para descargar un proveedor**

1.  Libere todos los punteros de interfaz que se mantienen en WMI cuando WMI llama al [**método Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de la interfaz principal del proveedor.

    Normalmente, un proveedor contiene punteros a las [**interfaces IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) proporcionadas en [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).

2.  Si la **propiedad Pure** de la instancia de [**\_ \_ Win32Provider**](--win32provider.md) asociada se establece en **FALSE,** el proveedor puede realizar la transición al rol de aplicación cliente después de que WMI llame a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Sin embargo, WMI no puede descargar un proveedor que funciona como sistema cliente, lo que aumenta la sobrecarga del sistema.

    Un proveedor con **pure** establecido en **TRUE** solo existe para las solicitudes de servicio. Por lo tanto, este tipo de proveedor no puede asumir el rol de una aplicación cliente y WMI puede descargarla.

## <a name="unloading-a-provider-during-shutdown"></a>Descargar un proveedor durante el apagado

En circunstancias normales, el uso de las instrucciones de Descargar un proveedor que también es un cliente WMI permite [que](#unloading-a-provider-that-is-also-a-wmi-client) WMI descargue el proveedor correctamente. Sin embargo, puede encontrarse con situaciones en las que WMI no puede seguir los procedimientos de descarga normales, como cuando el usuario decide apagar el sistema. Mediante el uso de un modelo de transacción de almacenamiento de datos, además de implementar una buena estrategia de limpieza, puede asegurarse de que el proveedor se descarga correctamente.

El usuario puede detener WMI en cualquier momento. En tal situación, WMI no descarga ningún proveedor ni llama al punto de [**entrada DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) en ningún proveedor en proceso. Además, si un proveedor en proceso se encuentra en medio de una llamada de método en el momento del cierre, WMI puede finalizar el subproceso en ejecución en medio de la llamada. En esta circunstancia, WMI no llama a rutinas que normalmente controlan la limpieza, como un destructor de objetos. Como máximo, WMI solo llamará [**a DllMain.**](/windows/desktop/Dlls/dllmain)

Cuando el sistema operativo apaga WMI, el sistema libera automáticamente toda la memoria asignada a un proveedor en proceso. El sistema operativo también cierra la mayoría de los recursos que mantiene el proveedor, como identificadores de archivo, identificadores de ventana, entre otros. El proveedor no necesita realizar ninguna acción específica para que esto suceda.

Dado que WMI puede apagarse en medio de una llamada, un proveedor no debe dejar los orígenes de datos en un estado incoherente. Dejar los datos en un estado incoherente no es un problema para los proveedores de solo lectura. Sin embargo, es posible que los proveedores con funcionalidades de escritura quieran implementar algún tipo de modelo de transacción para permitir una reversión segura después de una terminación brusca.

Aunque el sistema operativo puede liberar algunos recursos generales del sistema, el sistema no libera automáticamente todos los recursos. Por ejemplo, es posible que el sistema operativo no libere un socket o una conexión de base de datos. En su lugar, es posible que el proveedor tenga que limpiar manualmente estos recursos. Para evitar estos problemas, puede implementar el proveedor fuera de proceso o puede agregar código de limpieza.

La solución más sencilla es implementar el proveedor fuera de proceso. Un proveedor fuera de proceso no se cierra cuando WMI se cierra, aunque WMI liberará el proveedor después de un tiempo de espera COM. Los proveedores para los que los problemas de solidez de limpieza y finalización son más importantes que el rendimiento pueden estar fuera de proceso.

Si debe colocar el código de limpieza en el proveedor, tiene dos opciones. Un lugar para realizar este tipo de limpieza es [**DllMain**](/windows/desktop/Dlls/dllmain), la función de punto de entrada dll a la que llama el sistema operativo al descargar el archivo DLL. El código de limpieza se puede agregar directamente **a DllMain,** ejecutándose en respuesta a **DLL PROCESS \_ \_ DETACH**. Implementar código de limpieza **en DllMain** puede ser algo difícil de organizar, especialmente en entornos de programación como MFC o ATL. Para obtener más información, vea el artículo Microsoft Knowledge Base Q148791,*"How to Provide Your Own DllMain in an MFC Regular DLL.*" (Es posible que este recurso no esté disponible en algunos idiomas y países o regiones).

Como alternativa, también podría colocar el código de limpieza en el destructor de una clase global. Para obtener más información, vea Descargar un proveedor. El Windows operativo no asigna objetos globales en el montón. En su lugar, el sistema operativo llama a los destructores durante la descarga del archivo DLL.

A continuación se muestra un procedimiento de limpieza simple que podría caber dentro de un objeto global para WMI.


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



Hay muchas restricciones en cuanto a lo que se puede hacer en el código de limpieza con cualquier enfoque. Por ejemplo, no se puede acceder de ninguna manera a los subprocesos ni a los archivos DLL que no estén vinculados implícitamente. Además, no puede realizar llamadas COM en ninguna circunstancia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer descriptores de seguridad de namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
