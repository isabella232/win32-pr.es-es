---
title: Ejemplo de propiedad
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'Más información sobre: Ejemplo de propiedad'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f17e12031b326566e6b948b05dae5851ec4aabd1cc7fd0a0281fc9d1a89c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061645"
---
# <a name="property-sample"></a>Ejemplo de propiedad

En este tema se describe el ejemplo de código de ejemplo de propiedad. Contiene las secciones siguientes:

-   [Descripción](#description)
-   [Requisitos mínimos](#minimum-requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

El ejemplo de propiedad muestra cómo implementar tres estilos diferentes de hojas de propiedades: modal, modeless y wizard. También muestra cómo usar la función [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) para modificar el cuadro de diálogo de hoja de propiedades antes o después de crearlo.

## <a name="minimum-requirements"></a>Requisitos mínimos



| Producto          | Versión                              |
|------------------|--------------------------------------|
| Archivo DLL              | comctl32.dll versión 4.0             |
| Sistema operativo | Windows 95, Microsoft Windows NT 3.1 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

El ejemplo de propiedad se instala como parte de [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) y está disponible en la siguiente ubicación.



| Ubicación    | Ruta de acceso o dirección URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | %Archivos de programa% \\ SDK de Microsoft Windows número de versión Ejemplos de controles \\ \\ \[ \] \\ \\ winui \\ \\ comunes \\ |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo mediante el símbolo del sistema:

1.  Abra la ventana símbolo del sistema y vaya al directorio del proyecto.
2.  Escriba `msbuild [project file]`.

Para compilar el ejemplo mediante Visual Studio:

1.  Abra Windows explorador y vaya al directorio del proyecto.
2.  Haga doble clic en el icono del archivo .vcproj para abrir el proyecto en Visual Studio.
3.  En el **menú Compilar,** seleccione **Compilar solución** para compilar la solución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las hojas de propiedades](property-sheets.md)
</dt> </dl>

 

 




