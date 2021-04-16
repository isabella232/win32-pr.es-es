---
description: Accesos directos a páginas de referencia de DVD de C++
ms.assetid: b37337b7-b3be-4f49-b350-df5e3c88e3cf
title: Accesos directos a páginas de referencia de DVD de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7caed2aea59e41cf666c6ed63d220f986a8e36
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537564"
---
# <a name="shortcuts-to-c-dvd-reference-pages"></a>Accesos directos a páginas de referencia de DVD de C++

Las siguientes interfaces son las utilizadas normalmente al escribir una aplicación de DVD en C++.



| Interfaz                                    | Propósito                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) | Controla la presentación de subtítulos.                                                              |
| [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)                   | Se utiliza en técnicas avanzadas de sincronización de comandos para controlar un objeto de comando.                 |
| [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)         | Emite comandos para el filtro del [navegador de DVD](dvd-navigator-filter.md) (los métodos "SET").     |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) | Crea el gráfico de filtros de DVD.                                                                    |
| [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)               | Consulta el navegador del DVD para obtener información de estado e información sobre el disco (los métodos de "obtención"). |
| [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate)               | Guarda la información, como los marcadores, en el disco.                                                   |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)   | Controla el "recorrido de fotogramas" si el descodificador lo admite.                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



