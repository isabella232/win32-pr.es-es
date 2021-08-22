---
description: Representa una tableta conectada al equipo.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interfaz ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a0cb98a74758d701e7ab6322567d2a20606380a58fc43676ad5edb136cec999b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712255"
---
# <a name="itablet-interface"></a>Interfaz ITablet

Representa una tableta conectada al equipo.

## <a name="members"></a>Miembros

La **interfaz ITablet** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITablet** tiene estos métodos.



| Método                                                                 | Descripción                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateContext**](itablet-createcontext.md)                         | Crea un objeto de contexto que describe el dispositivo de tableta especificado.<br/>       |
| [**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | Recupera el objeto [**ITabletCursor**](itabletcursor.md) especificado.<br/>     |
| [**GetCursorCount**](itablet-getcursorcount.md)                       | Recupera el número de objetos de cursor asociados a la tableta.<br/>         |
| [**GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md) | Recupera la configuración de contexto predeterminada para la tableta.<br/>                     |
| [**GetHardwareCaps**](itablet-gethardwarecaps.md)                     | Recupera un valor que representa las funciones del hardware de tableta.<br/> |
| [**GetMaxInputRect**](itablet-getmaxinputrect.md)                     | Recupera un rectángulo que representa el área de entrada máxima de la tableta.<br/>    |
| [**GetName**](itablet-getname.md)                                     | Recupera una cadena que contiene el nombre del dispositivo de tableta.<br/>               |
| [**GetPlugAndPlayId**](itablet-getplugandplayid.md)                   | Recupera una cadena que contiene el identificador de Plug and Play para el dispositivo de tableta.<br/>  |
| [**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | Recupera los datos de métricas de una propiedad especificada.<br/>                       |



 

## <a name="remarks"></a>Comentarios

Los desarrolladores no deben usar esta interfaz.

En el código siguiente se describe cómo se define la interfaz **ITablet.**

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

