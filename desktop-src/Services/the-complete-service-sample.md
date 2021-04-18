---
description: 'Más información sobre: el ejemplo de servicio completo'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: El ejemplo de servicio completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668183"
---
# <a name="the-complete-service-sample"></a>El ejemplo de servicio completo

Los temas de esta sección forman un ejemplo de servicio completo:

-   [Sample.MC](sample-mc.md) (contiene mensajes de error)
-   [SVC. cpp](svc-cpp.md) (contiene el código de servicio)
-   [SvcConfig. cpp](svcconfig-cpp.md) (contiene código de configuración de servicio)
-   [SvcControl. cpp](svccontrol-cpp.md) (contiene el código de control de servicio)

## <a name="building-the-service"></a>Compilar el servicio

En el procedimiento siguiente se describe cómo crear el servicio y registrar el archivo DLL del mensaje de evento.

**Para generar el servicio y registrar el archivo DLL del mensaje de evento**

1.  Cree el archivo DLL de mensajes desde Sample.mc mediante los pasos siguientes:
    1.  **MC-U sample.mc**
    2.  **RC-r sample. RC**
    3.  **Link-dll-NOENTRY -out:sample.dll sample. res**
2.  Cree Svc.exe, SvcConfig.exe y SvcControl.exe de SVC. cpp, SvcConfig. cpp y SvcControl. cpp, respectivamente.
3.  Cree la clave del registro **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** y agregue los siguientes valores del registro a esta clave.

    | Value                              | Tipo       | Descripción                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *\_ ruta de acceso de dll* | Registro \_ SZ    | La ruta de acceso al archivo DLL de solo recurso que contiene cadenas que el servicio puede escribir en el registro de eventos.               |
    | **TypesSupported** = 0x00000007    | \_valor DWORD reg | Máscara de bits que especifica los tipos de evento admitidos. El valor 0x000000007 indica que se admiten todos los tipos. |

    

     

## <a name="testing-the-service"></a>Probar el servicio

En el procedimiento siguiente se describe cómo probar el servicio.

**Para probar el servicio**

1.  En el panel de control, inicie la aplicación **servicios** . (En los pasos siguientes, use la tecla F5 para actualizar la pantalla después de ejecutar un comando que modifique la información en la aplicación **servicios** ).
2.  Ejecute el siguiente comando para instalar el servicio:

    **instalación de SVC**

    El servicio escribe "el servicio se instaló correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.

    Si la instalación del servicio se realiza correctamente, el servicio se muestra en la aplicación **servicios** . Tenga en cuenta que name se establece en "SvcName", la **Descripción** y el **Estado** están en blanco y **el** **tipo de inicio** se establece en "manual".

3.  Ejecute el siguiente comando para iniciar el servicio:

    **svccontrol Start SvcName**

    Si la operación se realiza correctamente, el programa de control de servicio escribe "el inicio del servicio está pendiente..." y, a continuación, "el servicio se inició correctamente" en la consola. De lo contrario, el programa escribe un mensaje de error en la consola.

    Si el servicio se inicia correctamente, el **Estado** se establece en "iniciado". El código de la función [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) lo ejecuta el SCM. Si se produce un error, el servicio escribirá un mensaje de error en el registro de eventos. Este mensaje incluye el nombre de la función que produjo un error y el código de error que se devolvió en caso de error.

4.  Ejecute el siguiente comando para actualizar la descripción del servicio:

    **svcconfig describir SvcName**

    El programa de configuración de servicio escribe "Descripción del servicio actualizada correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.

    Si la actualización se realiza correctamente, la **Descripción** se establece en "esta es una descripción de la prueba".

5.  Ejecute el siguiente comando para consultar la configuración del servicio:

    **SvcName consulta svcconfig**

    El programa de configuración del servicio escribe la información de configuración del servicio en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.

6.  Ejecute el siguiente comando para cambiar la DACL de servicio:

    **svccontrol DACL SvcName**

    El programa de configuración del servicio escribe "DACL del servicio se actualizó correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.

7.  Ejecute el siguiente comando para deshabilitar el servicio:

    **svcconfig deshabilitar SvcName**

    El programa de configuración del servicio escribe "servicio deshabilitado correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.

    Si el servicio se deshabilita correctamente, el **tipo de inicio** se establece en "deshabilitado".

8.  Ejecute el siguiente comando para habilitar el servicio:

    **svcconfig habilitar SvcName**

    El programa de configuración del servicio escribe "servicio habilitado correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.

    Si el servicio se habilita correctamente, el **tipo de inicio** se establece en "manual".

9.  Ejecute el siguiente comando para detener el servicio:

    **svccontrol detener SvcName**

    Si la operación se realiza correctamente, el programa de control de servicio escribe "servicio detenido pendiente..." y, a continuación, "el servicio se detuvo correctamente" en la consola. De lo contrario, el programa escribe un mensaje de error en la consola.

    Si el servicio se detiene correctamente, el **Estado** es en blanco.

    Si no se puede detener el servicio, el programa de control de servicio escribe un mensaje de error en el registro de eventos que incluye el nombre de la función en la que se produjo el error y el código de error devuelto en caso de error.

10. Ejecute el siguiente comando para eliminar el servicio:

    **svcconfig eliminar SvcName**

    El programa de configuración de servicio escribe "el servicio se eliminó correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.

    Si el servicio se elimina correctamente, ya no se muestra en la aplicación **servicios** . (Tenga en cuenta que si intenta eliminar un servicio que no está detenido, la operación se realiza correctamente, pero el **tipo de inicio** se establece en "deshabilitado" y la entrada del servicio se eliminará al reiniciar el sistema o cuando el servicio finalice con el administrador de tareas.)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de servicios](using-services.md)
</dt> </dl>

 

 
