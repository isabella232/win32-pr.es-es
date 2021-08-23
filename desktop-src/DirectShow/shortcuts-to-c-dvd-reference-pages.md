---
description: Accesos directos a páginas de referencia de DVD de C++
ms.assetid: b37337b7-b3be-4f49-b350-df5e3c88e3cf
title: Accesos directos a páginas de referencia de DVD de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fa7d2f78b7bbdfbcbfa5c71a91034a19b108b2f785cf3cec47017e46d6d7f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583265"
---
# <a name="shortcuts-to-c-dvd-reference-pages"></a>Accesos directos a páginas de referencia de DVD de C++

Las interfaces siguientes son las que se usan normalmente al escribir una aplicación de DVD en C++.



| Interfaz                                    | Propósito                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) | Controla la presentación de subtítulos.                                                              |
| [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)                   | Se usa en técnicas avanzadas de sincronización de comandos para controlar un objeto de comando.                 |
| [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)         | Emite comandos para el filtro [DVD Navigator](dvd-navigator-filter.md) (los métodos "set").     |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) | Crea el gráfico de filtro de DVD.                                                                    |
| [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)               | Consulta el navegador de DVD para obtener información de estado e información sobre el disco (los métodos "get"). |
| [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate)               | Guarda información, como marcadores, en el disco.                                                   |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)   | Controla el "paso a paso del marco" si el descodificador lo admite.                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



