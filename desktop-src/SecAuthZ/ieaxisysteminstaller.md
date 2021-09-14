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
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160821"
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

## <a name="members"></a>Members

La **interfaz IeAxiSystemInstaller** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiSystemInstaller también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IeAxiSystemInstaller tiene** estos métodos.



| Método                                                                              | Descripción                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Instala el objeto ActiveX especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller se define como a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



 

