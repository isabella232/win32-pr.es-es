---
title: Personalización de una miniatura icónica y un mapa de bits de vista previa dinámica
description: Muestra cómo personalizar una miniatura de iconos y un mapa de bits de vista previa dinámica (también denominado vista previa de inspección).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718590"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a>Personalización de una miniatura icónica y un mapa de bits de vista previa dinámica

## <a name="description"></a>Descripción

Puede personalizar una miniatura de iconos y un mapa de bits de *vista previa dinámica* (o *vista previa de PEEK*) mediante el uso de funciones y mensajes que se introducen en las api de Windows 7 administrador de ventanas de escritorio (DWM).

En concreto, use la función [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) y el [**mensaje \_ SENDICONICTHUMBNAILBITMAP de WM**](wm-dwmsendiconicthumbnail.md) para personalizar una miniatura de iconos. También puede usar la función [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) y el mensaje [**de \_ SENDICONICLIVEPREVIEWBITMAP de WM**](wm-dwmsendiconiclivepreviewbitmap.md) para establecer un mapa de bits de vista previa de iconos dinámicos.

Para obtener una aplicación de ejemplo que usa la función **DwmSetIconicThumbnail** , vea el [ejemplo TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).

En la ilustración siguiente se muestra una miniatura predeterminada transformada en una miniatura personalizada.

![Ilustración de una imagen en miniatura original y una imagen de miniatura modificada con un mapa de bits personalizado](images/customthumbnail.jpg)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 7 o Windows Vista con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Vista                          |
| Servidor mínimo compatible | Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Server 2008 |
| Windows SDK mínimo      | [Kit de desarrollo de software (SDK) de Windows para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a>Compilación del ejemplo TabThumbnails

**Para compilar el ejemplo mediante Microsoft Visual Studio (método preferido)**

1.  Abra el explorador de Windows y vaya a la carpeta donde se encuentra el archivo TabThumbnails. sln.
2.  Haga doble clic en el archivo de solución (. sln) para abrir el archivo en Microsoft Visual Studio.
3.  En el menú **Compilar** , haga clic en **Compilar solución**. La aplicación se genera en el \\ Directorio de depuración o \\ versión predeterminado.

**Para generar el ejemplo mediante el símbolo del sistema**

1.  Abra una ventana del símbolo del sistema y vaya al directorio de ejemplo.
2.  Escriba `msbuild TabThumbnails.sln`.

## <a name="related-topics"></a>Temas relacionados

[Administrador de ventanas de escritorio](dwm-overview.md)

[Desarrollo de Windows](/windows/desktop/win32-and-com-development)
