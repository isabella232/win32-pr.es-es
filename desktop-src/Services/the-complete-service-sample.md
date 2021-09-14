---
description: 'Más información sobre: Ejemplo de servicio completo'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Ejemplo de servicio completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170781"
---
# <a name="the-complete-service-sample"></a>Ejemplo de servicio completo

Los temas de esta sección forman un ejemplo de servicio completo:

-   [Sample.mc](sample-mc.md) (contiene mensajes de error)
-   [Svc.cpp](svc-cpp.md) (contiene el código de servicio)
-   [SvcConfig.cpp](svcconfig-cpp.md) (contiene el código de configuración del servicio)
-   [SvcControl.cpp](svccontrol-cpp.md) (contiene código de control de servicio)

## <a name="building-the-service"></a>Compilar el servicio

En el procedimiento siguiente se describe cómo compilar el servicio y registrar el archivo DLL del mensaje de evento.

**Para compilar el servicio y registrar el archivo DLL del mensaje de evento**

1.  Compile el archivo DLL de mensaje Sample.mc mediante los pasos siguientes:
    1.  **mc -U sample.mc**
    2.  **rc -r sample.rc**
    3.  **link -dll -noentry -out:sample.dll sample.res**
2.  Compile Svc.exe, SvcConfig.exe y SvcControl.exe desde Svc.cpp, SvcConfig.cpp y SvcControl.cpp, respectivamente.
3.  Cree la clave del Registro **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services \\ EventLog Application \\ \\ SvcName** y agregue los siguientes valores del Registro a esta clave.

    | Value                              | Tipo       | Descripción                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *ruta de acceso de \_ dll* | REG \_ SZ    | Ruta de acceso al archivo DLL de solo recursos que contiene cadenas que el servicio puede escribir en el registro de eventos.               |
    | **TypesSupported** = 0x00000007    | REG \_ DWORD | Máscara de bits que especifica los tipos de eventos admitidos. El valor 0x000000007 indica que se admiten todos los tipos. |

    

     

## <a name="testing-the-service"></a>Probar el servicio

En el procedimiento siguiente se describe cómo probar el servicio.

**Para probar el servicio**

1.  En Panel de control, inicie la **aplicación Servicios.** (En los pasos siguientes, use la tecla F5 para actualizar la pantalla después de ejecutar un comando que modifica la información en la **aplicación Servicios).**
2.  Ejecute el siguiente comando para instalar el servicio:

    **svc install**

    El servicio escribe "Servicio instalado correctamente" en la consola si la operación se realiza correctamente o un mensaje de error en caso contrario.

    Si la instalación del servicio se realiza correctamente, el servicio se muestra en la **aplicación** Servicios. Tenga en cuenta **que Nombre** está establecido  en "SvcName", **Descripción** y Estado están en blanco y **Tipo** de inicio está establecido en "Manual".

3.  Ejecute el siguiente comando para iniciar el servicio:

    **svccontrol start SvcName**

    Si la operación se realiza correctamente, el programa de control de servicio escribe "Inicio del servicio pendiente..." y, a continuación, "El servicio se inició correctamente" en la consola. De lo contrario, el programa escribe un mensaje de error en la consola.

    Si el servicio se inicia correctamente, **El** estado se establece en "Iniciado". El SCM ejecuta el código de la función [*ServiceMain.*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) Si se produce un error, el servicio escribirá un mensaje de error en el registro de eventos. Este mensaje incluye el nombre de la función que produjo el error y el código de error devuelto en caso de error.

4.  Ejecute el siguiente comando para actualizar la descripción del servicio:

    **svcconfig describe SvcName**

    El programa de configuración del servicio escribe "Descripción del servicio actualizada correctamente" en la consola si la operación se realiza correctamente o un mensaje de error en caso contrario.

    Si la actualización se realiza correctamente, **Description** se establece en "This is a test description" (Esta es una descripción de prueba).

5.  Ejecute el siguiente comando para consultar la configuración del servicio:

    **svcconfig query SvcName**

    El programa de configuración de servicio escribe la información de configuración del servicio en la consola si la operación se realiza correctamente o un mensaje de error en caso contrario.

6.  Ejecute el siguiente comando para cambiar la DACL del servicio:

    **svccontrol dacl SvcName**

    El programa de configuración de servicio escribe "DACL de servicio actualizada correctamente" en la consola si la operación se realiza correctamente o un mensaje de error en caso contrario.

7.  Ejecute el siguiente comando para deshabilitar el servicio:

    **svcconfig disable SvcName**

    El programa de configuración del servicio escribe "Servicio deshabilitado correctamente" en la consola si la operación se realiza correctamente o un mensaje de error en caso contrario.

    Si el servicio se deshabilita correctamente, **tipo de** inicio se establece en "Deshabilitado".

8.  Ejecute el siguiente comando para habilitar el servicio:

    **svcconfig enable SvcName**

    El programa de configuración del servicio escribe "Servicio habilitado correctamente" en la consola si la operación se realiza correctamente o un mensaje de error en caso contrario.

    Si el servicio se habilita correctamente, **tipo de inicio** se establece en "Manual".

9.  Ejecute el siguiente comando para detener el servicio:

    **svccontrol stop SvcName**

    Si la operación se realiza correctamente, el programa de control de servicio escribe "Service stop pending..." y, a continuación, "El servicio se detuvo correctamente" en la consola. De lo contrario, el programa escribe un mensaje de error en la consola.

    Si el servicio se detiene correctamente, **el estado está** en blanco.

    Si el servicio no se puede detener, el programa de control de servicio escribe un mensaje de error en el registro de eventos que incluye el nombre de la función que produjo un error y el código de error devuelto en caso de error.

10. Ejecute el siguiente comando para eliminar el servicio:

    **svcconfig delete SvcName**

    El programa de configuración del servicio escribe "Servicio eliminado correctamente" en la consola si la operación se realiza correctamente o un mensaje de error en caso contrario.

    Si el servicio se elimina correctamente, ya no se muestra en la **aplicación** Servicios. (Tenga en cuenta que si intenta eliminar un servicio que  no está detenido, la operación se realiza correctamente, pero tipo de inicio está establecido en "Deshabilitado" y la entrada del servicio se eliminará al reiniciar el sistema o cuando el servicio finalice mediante Administrador de tareas).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de servicios](using-services.md)
</dt> </dl>

 

 
