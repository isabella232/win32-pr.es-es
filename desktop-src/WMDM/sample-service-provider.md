---
title: Proveedor de servicios de ejemplo
description: Proveedor de servicios de ejemplo
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Media Administrador de dispositivos,samples
- Administrador de dispositivos,samples
- Windows Ejemplo Administrador de dispositivos, proveedor de servicios
- Administrador de dispositivos,ejemplo de proveedor de servicios
- proveedores de servicios, ejemplos
- samples,service providers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474575"
---
# <a name="sample-service-provider"></a>Proveedor de servicios de ejemplo

El SDK Windows Media Administrador de dispositivos incluye un proveedor de servicios de ejemplo para su uso. Este proveedor de servicios incluye una clase que informa de cada unidad de disco duro del equipo como si fuera un dispositivo conectado. La única aplicación que usará este proveedor de servicios es la aplicación de ejemplo. Windows El Explorador no verá los "dispositivos" notificados por este proveedor de servicios. El ejemplo del proveedor de servicios es un objeto COM basado en ATL. En los pasos siguientes se explica cómo usar el proveedor de servicios de ejemplo:

> [!Note]  
> El proveedor de servicios de ejemplo implementa muy pocas características, por lo que no debe usarse para probar Windows aplicaciones Administrador de dispositivos multimedia. Para probar una aplicación, use un proveedor de servicios totalmente implementado.

 

-   El ejemplo se envió con un error de codificación que hará que el proveedor de servicios no funcione correctamente. Para corregir este error, abra el archivo MDSPEnumStorage.cpp instalado en la carpeta ruta de instalación del *SDK* de <  > \\ WMFSDK95 \\ WMDM \\ mdsp mshdsp, vaya a la línea \\ 185 y cambie la línea siguiente:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

Por esta otra:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Compile el MsHDSP.dll archivo. Puede hacerlo mediante NMAKE o Visual Studio. Consulte [Compilación del proveedor de servicios](compiling-the-sample-service-provider-using-nmake.md) de ejemplo mediante NMAKE o Compilación del proveedor de servicios de ejemplo mediante [Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) para obtener información sobre cómo compilar la aplicación.
2.  Registre MsHDSP.dll con regsvr32. La siguiente línea, que se escribe en una ventana del símbolo del sistema en la misma carpeta que MsHDSP.dll, registrará el proveedor de servicios de ejemplo:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Para detener la suplantación de un dispositivo, escriba la siguiente línea en el símbolo del sistema:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  La aplicación de ejemplo que se incluye con este SDK solo puede ver los dispositivos extraíbles suplantados por este archivo DLL. Compile la aplicación de ejemplo mediante uno de los métodos descritos en [Aplicación de escritorio de ejemplo](sample-desktop-application.md).
4.  Para depurar el proveedor de servicios con Visual Studio, abra el proveedor de servicios en Visual Studio seleccione **Iniciar** en el **menú** Depurar. En el cuadro de diálogo emergente, vaya a la aplicación de ejemplo que creó en el paso anterior y haga clic en Aceptar y el proveedor de servicios comenzará a ejecutarse en modo de depuración.

    Para ejecutar el proveedor de servicios sin depurar en Visual Studio, simplemente registre el msdhsp.dll y ejecute la aplicación de escritorio de ejemplo que se incluye con el SDK. La aplicación de escritorio de ejemplo ejecuta automáticamente el proveedor de servicios de ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Muestras**](samples.md)
</dt> </dl>

 

 




