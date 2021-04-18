---
title: Proveedor de servicios de ejemplo
description: Proveedor de servicios de ejemplo
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de proveedor de servicios
- Administrador de dispositivos, ejemplo de proveedor de servicios
- proveedores de servicios, ejemplos
- ejemplos, proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695329"
---
# <a name="sample-service-provider"></a>Proveedor de servicios de ejemplo

El SDK de Windows Media Administrador de dispositivos incluye un proveedor de servicios de ejemplo para su uso. Este proveedor de servicios incluye una clase que informa de cada unidad de disco duro del equipo como si fuera un dispositivo conectado. La única aplicación que utilizará este proveedor de servicios es la aplicación de ejemplo; El explorador de Windows no verá los dispositivos "devueltos por este proveedor de servicios". El ejemplo de proveedor de servicios es un objeto COM compilado en ATL. En los pasos siguientes se explica cómo usar el proveedor de servicios de ejemplo:

> [!Note]  
> El proveedor de servicios de ejemplo implementa muy pocas características, por lo que no debe usarse para probar aplicaciones de Windows Media Administrador de dispositivos. Para probar una aplicación, utilice un proveedor de servicios totalmente implementado.

 

-   El ejemplo se ha enviado con un error de codificación que hará que el proveedor de servicios no funcione correctamente. Para corregir este error, abra el archivo MDSPEnumStorage. cpp instalado en la carpeta < *ruta de instalación del SDK*  > \\ WMFSDK95 \\ WMDM \\ mdsp \\ mshdsp, vaya a la línea 185 y cambie la línea siguiente:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

Por esta otra:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Compile el archivo de MsHDSP.dll. Puede hacerlo mediante NMAKE o Visual Studio. Vea [compilar el proveedor de servicios de ejemplo con NMAKE](compiling-the-sample-service-provider-using-nmake.md) o [compilar el proveedor de servicios de ejemplo con Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) para obtener información sobre cómo compilar la aplicación.
2.  Registre MsHDSP.dll mediante regsvr32. En la línea siguiente, escrita en una ventana del símbolo del sistema en la misma carpeta que MsHDSP.dll, se registrará el proveedor de servicios de ejemplo:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Para detener la suplantación de un dispositivo, escriba la siguiente línea en el símbolo del sistema:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  Los dispositivos extraíbles suplantados por este archivo DLL solo pueden verse en la aplicación de ejemplo que se incluye con este SDK. Compile la aplicación de ejemplo mediante uno de los métodos descritos en [aplicación de escritorio de ejemplo](sample-desktop-application.md).
4.  Para depurar el proveedor de servicios con Visual Studio, abra el proveedor de servicios en Visual Studio y seleccione **iniciar** en el menú **depurar** . En el cuadro de diálogo emergente, vaya a la aplicación de ejemplo que creó en el paso anterior y haga clic en **Aceptar**, y el proveedor de servicios comenzará a ejecutarse en modo de depuración.

    Para ejecutar el proveedor de servicios sin depurar en Visual Studio, basta con registrar el msdhsp.dll y ejecutar la aplicación de escritorio de ejemplo que se incluye con el SDK. La aplicación de escritorio de ejemplo ejecuta el proveedor de servicios de ejemplo automáticamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos**](samples.md)
</dt> </dl>

 

 




