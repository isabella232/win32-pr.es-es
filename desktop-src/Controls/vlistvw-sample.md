---
title: Ejemplo de VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Más información sobre: Ejemplo VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefcd39c44e79ab4eec23f7becf202d1a3cd3566f6be9496e9fd61b577c87f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957564"
---
# <a name="vlistvw-sample"></a>Ejemplo de VListVW

En este tema se describe el ejemplo de código de ejemplo VListVW. Contiene las secciones siguientes:

-   [Descripción](#description)
-   [Requisitos mínimos](#minimum-requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

El ejemplo VListVW muestra cómo implementar un control simple de vista de lista virtual en una aplicación. Un control de vista de lista virtual es un control list-view estándar con el **estilo \_ OWNERDATA de LVS.** En este ejemplo se crea un control de vista de lista que contiene "virtualmente" 100 000 elementos. Los elementos nunca se agregan realmente. En su lugar, se "indica" al control de vista de lista virtual cuántos elementos contiene con el [**mensaje \_ LVM SETITEMCOUNT.**](lvm-setitemcount.md) Cuando es necesario dibujar un elemento, el control list-view consulta la ventana primaria para ver información con la notificación [ \_ LVN GETDISPINFO.](lvn-getdispinfo.md)

## <a name="minimum-requirements"></a>Requisitos mínimos



| Producto          | Versión                               |
|------------------|---------------------------------------|
| Archivo DLL              | comctl32.dll versión 4.70             |
| Sistema operativo | Windows 95, Microsoft Windows NT 3.51 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

El ejemplo VListVW está disponible en en github en el [repositorio Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples)de . Los ejemplos de elementos de control de vista de lista se pueden encontrar [aquí](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)

 

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

[Acerca de List-View controles](list-view-controls-overview.md)
</dt> </dl>

 

 




