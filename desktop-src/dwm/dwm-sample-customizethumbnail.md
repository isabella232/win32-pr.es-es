---
title: Personalización de una miniatura icónica y un mapa de bits de vista previa dinámica
description: Muestra cómo personalizar una miniatura y un mapa de bits de vista previa en directo (también denominado vista previa de Peek).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 94fa65fd4cd80f837867a6a5d225ec43050cf0018c8116e8beae099ed1067025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022174"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a>Personalización de una miniatura icónica y un mapa de bits de vista previa dinámica

## <a name="description"></a>Descripción

Puede personalizar una miniatura y un mapa de bits de vista previa en directo *(o* Vista previa *de* Peek) mediante funciones y mensajes que se introducen en las API de Windows 7 Administrador de ventanas de escritorio (DWM).

En concreto, se usa la [**función DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) y el mensaje [**WM \_ SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) para personalizar una miniatura icono. También puede usar la [**función DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) y el mensaje [**WM \_ SENDICONICLIVEPREVIEWBITMAP para**](wm-dwmsendiconiclivepreviewbitmap.md) establecer un mapa de bits de vista previa en directo icono.

Para obtener una aplicación de ejemplo que usa la **función DwmSetIconicThumbnail,** vea [Ejemplo de TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).

En la ilustración siguiente se muestra una miniatura predeterminada transformada en una miniatura personalizada.

![ilustración de una imagen en miniatura original y una imagen en miniatura modificada con un mapa de bits personalizado](images/customthumbnail.jpg)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 7 o Windows Vista con Service Pack 2 (SP2) y actualización de plataforma para Windows Vista                          |
| Servidor mínimo compatible | Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y actualización de plataforma para Windows Server 2008 |
| SDK Windows mínimo      | [Windows Kit de desarrollo de software (SDK) para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a>Creación del ejemplo TabThumbnails

**Para compilar el ejemplo mediante Microsoft Visual Studio (método preferido)**

1.  Abra Windows Explorer y vaya a la carpeta donde se encuentra el archivo TabThumbnails.sln.
2.  Haga doble clic en el archivo de solución (.sln) para abrir el archivo en Microsoft Visual Studio.
3.  En el menú **Compilar** , haga clic en **Compilar solución**. La aplicación se compila en el directorio \\ debug o \\ release predeterminado.

**Para compilar el ejemplo mediante el símbolo del sistema**

1.  Abra una ventana del símbolo del sistema y vaya al directorio de ejemplo.
2.  Escriba `msbuild TabThumbnails.sln`.

## <a name="related-topics"></a>Temas relacionados

[Administrador de ventanas de escritorio](dwm-overview.md)

[Desarrollo de Windows](/windows/desktop/win32-and-com-development)
