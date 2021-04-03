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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083253"
---
# <a name="ieaxisysteminstaller-interface"></a>Interfaz IeAxiSystemInstaller

La interfaz **IeAxiSystemInstaller** instala un objeto ActiveX.

Esta interfaz no está declarada en un encabezado público. Las aplicaciones deben definirla. El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.

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

La interfaz **IeAxiSystemInstaller** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiSystemInstaller** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IeAxiSystemInstaller** tiene estos métodos.



| Método                                                                              | Descripción                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Instala el objeto ActiveX especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller se define como a50ea6f8-4764-4299-B309-022b2a8b4d8d<br/>                   |



 

