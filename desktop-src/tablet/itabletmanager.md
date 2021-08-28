---
description: Proporciona acceso a todas las tabletas conectadas al equipo.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Interfaz ITabletManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ae4a12964ff900d8a30c0f59d2210c82007995337a2661a6fbd29a6acdfccdf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820525"
---
# <a name="itabletmanager-interface"></a>Interfaz ITabletManager

Proporciona acceso a todas las tabletas conectadas al equipo.

## <a name="members"></a>Miembros

La **interfaz ITabletManager** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletManager** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITabletManager** tiene estos métodos.



| Método                                                  | Descripción                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))           | Recupera el objeto de tableta especificado.<br/>                  |
| [**GetTabletCount**](itabletmanager-gettabletcount.md) | Recupera el número de tabletas conectadas al sistema.<br/> |



 

## <a name="remarks"></a>Comentarios

Los desarrolladores no deben usar esta interfaz.

El código siguiente muestra cómo se implementa la interfaz **ITabletManager.**

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un identificador de clase de CLSID TabletManagerS y, a continuación, llame a QueryInterface para obtener un puntero a la \_ interfaz **ITabletManager**. [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) El GUID de \_ CLSID TabletManagerS se define de la siguiente manera:

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

