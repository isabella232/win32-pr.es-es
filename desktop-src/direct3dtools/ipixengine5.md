---
description: Extensiones de la interfaz IPixEngine4 que contienen adiciones para ver texturas.
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixEngine5
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c52f22108b4a1b9b8576518801fc5e9896f28fa
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787149"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span id="vspixengine.ipixengine5"></span>Interfaz IPixEngine5

Extensiones de la interfaz IPixEngine4 que contienen adiciones para ver texturas.

## <a name="members"></a>Members

La **interfaz IPixEngine5** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixEngine5** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

La **interfaz IPixEngine5** tiene estos métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descripción</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></td><td ><p>Libera una textura y notifica al host de forma asincrónica.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></td><td ><p>Solicitud asincrónica para cargar datos de histograma.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></td><td ><p>Carga una textura de un archivo y notifica al host de forma asincrónica cuando se completa.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></td><td ><p>Carga un segmento de textura y notifica al host de forma asincrónica cuando se completa.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></td><td ><p>Lee un valor de textura y devuelve el resultado al host de forma asincrónica.</p></td></tr><tr class="even"><td ><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></td><td ><p>Representa una textura en un archivo y devuelve el resultado al host de forma asincrónica.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></td><td ><p>Guarda una textura.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
