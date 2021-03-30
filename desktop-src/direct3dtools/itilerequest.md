---
description: Solicitud de una textura en mosaico que se escribirá como un archivo DDS.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz ITileRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ceb630661cfe67bc8beb28b2d1de2480726ec594
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806253"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span id="vspixengine.itilerequest"></span>Interfaz ITileRequest

Solicitud de una textura en mosaico que se escribirá como un archivo DDS.

## <a name="members"></a>Miembros

La interfaz **ITileRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITileRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La interfaz **ITileRequest** tiene estos métodos.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Método</th><th style="text-align: left;">Descripción</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></td><td style="text-align: left;"><p>Solicita obtener el contenido sin procesar de un icono.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></td><td style="text-align: left;"><p>Solicita que obtenga el contenido de una textura en mosaico como. Archivo DDS (DirectDraw Surface).</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
