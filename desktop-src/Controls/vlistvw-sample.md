---
title: Ejemplo de VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Más información acerca de: ejemplo VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659669"
---
# <a name="vlistvw-sample"></a>Ejemplo de VListVW

En este tema se describe el ejemplo de código de ejemplo VListVW. Contiene las secciones siguientes:

-   [Descripción](#description)
-   [Requisitos mínimos](#minimum-requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En el ejemplo VListVW se muestra cómo implementar un control de vista de lista virtual simple en una aplicación. Un control de vista de lista virtual es un control de vista de lista estándar con el estilo **LVS \_ OWNERDATA** . En este ejemplo se crea un control de vista de lista que "prácticamente" contiene 100.000 elementos. Los elementos nunca se agregan realmente. En su lugar, el control de vista de lista virtual se "indica" el número de elementos que contiene con el mensaje [**\_ SETITEMCOUNT de LVM**](lvm-setitemcount.md) . Cuando es necesario dibujar un elemento, el control de vista de lista consulta la información de presentación de la ventana primaria con la notificación [ \_ GETDISPINFO de LVN](lvn-getdispinfo.md) .

## <a name="minimum-requirements"></a>Requisitos mínimos



| Producto          | Versión                               |
|------------------|---------------------------------------|
| Archivo DLL              | comctl32.dll versión 4,70             |
| Sistema operativo | Windows 95, Microsoft Windows NT 3,51 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

El ejemplo VListVW está disponible en github en el [repositorio de ejemplos de Windows clásico](https://github.com/microsoft/Windows-classic-samples). Los ejemplos de elementos de control de vista de lista se pueden encontrar [aquí](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw) .

 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo mediante el símbolo del sistema:

1.  Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto.
2.  Escriba `msbuild [project file]`.

Para compilar el ejemplo con Visual Studio:

1.  Abra el explorador de Windows y navegue hasta el directorio del proyecto.
2.  Haga doble clic en el icono del archivo. vcproj para abrir el proyecto en Visual Studio.
3.  En el menú **compilar** , seleccione **compilar solución** para compilar la solución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles List-View](list-view-controls-overview.md)
</dt> </dl>

 

 




