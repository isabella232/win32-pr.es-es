---
description: DMOEnum Sample
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: DMOEnum Sample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375227"
---
# <a name="dmoenum-sample"></a>DMOEnum Sample

## <a name="description"></a>Descripción

Esta aplicación de ejemplo enumera todos los objetos multimedia [directX](directx-media-objects.md) (DMO) registrados en el sistema del usuario y muestra información sobre ellos.

El ejemplo usa la [**función DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) y la [**interfaz IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) para enumerar las DDO. Usa la [**interfaz IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) y otras interfaces DMO para recuperar información sobre cada DMO.

## <a name="usage"></a>Uso

Cuando se inicia la aplicación, enumera todas las DDO instaladas. Si selecciona una categoría de DMO, la aplicación muestra solo las DDO de esa categoría. Para ver información sobre un DMO, seleccione el DMO de la lista. La aplicación muestra el número de secuencias, los tipos de medios preferidos, el servidor DLL para ese DMO y otra información sobre el DMO. Para incluir o excluir las DDO con clave, active **la casilla Include Keyed DMOs?** (¿Incluir DDO con clave?).

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente [de Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: *\[ SDK Root \]* Samples Multimedia DirectShow \\ \\ \\ \\ Misc \\ DMOEnum.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



