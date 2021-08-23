---
description: Instala un objeto ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interfaz IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: fb462c4b4f8fc28d9d00de230dea1bbd3670c4fb6eaa962d59875b4fd9054c8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671015"
---
# <a name="ieaxisysteminstaller-interface"></a>Interfaz IeAxiSystemInstaller

La **interfaz IeAxiSystemInstaller** instala un ActiveX objeto .

Esta interfaz no se declara en un encabezado público. Las aplicaciones deben definirla por sí mismas. El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a>Miembros

La **interfaz IeAxiSystemInstaller** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiSystemInstaller también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IeAxiSystemInstaller tiene** estos métodos.



| Método                                                                              | Descripción                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Instala el objeto ActiveX especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller se define como a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



 

