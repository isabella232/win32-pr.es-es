---
description: Ejemplo de DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Ejemplo de DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274787"
---
# <a name="dmoenum-sample"></a>Ejemplo de DMOEnum

## <a name="description"></a>Descripción

En esta aplicación de ejemplo se enumeran todos los [objetos multimedia de DirectX](directx-media-objects.md) (DMOs) registrados en el sistema del usuario y se muestra información sobre ellos.

En el ejemplo se usa la función [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) y la interfaz [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) para enumerar el DMOs. Usa la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) y otras interfaces de DMO para recuperar información acerca de cada DMO.

## <a name="usage"></a>Uso

Cuando se inicia la aplicación, enumera todas las DMOs instaladas. Si selecciona una categoría de DMO específica, la aplicación muestra solo los DMOs de esa categoría. Para ver información acerca de un DMO, seleccione el DMO en la lista. La aplicación muestra el número de flujos, los tipos de medios preferidos, el servidor DLL para ese DMO y otra información acerca de DMO. Para incluir o excluir DMOs con clave, active la casilla **incluir DMOs con clave** .

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ multimedia \\ DirectShow \\ varios \\ DMOEnum.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



