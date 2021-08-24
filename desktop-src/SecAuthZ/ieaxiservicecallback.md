---
description: Lo llama la interfaz IeAxiSystemInstaller para comprobar que se puede ActiveX un objeto .
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: IeAxiServiceCallback (interfaz)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3313a1744a1fb9a3b34549ca32bb9b0c7cf18977c7785075900c4a11425b5949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908355"
---
# <a name="ieaxiservicecallback-interface"></a>IeAxiServiceCallback (interfaz)

La interfaz [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) llama a la interfaz **IeAxiServiceCallback** para comprobar que se puede instalar ActiveX objeto .

La [**clase CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa esta interfaz.

Esta interfaz no se declara en un encabezado público. Las aplicaciones deben definirla ellos mismos. El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a>Miembros

La **interfaz IeAxiServiceCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiServiceCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IeAxiServiceCallback tiene** estos métodos.



| Método                                                | Descripción                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**VerifyFile**](ieaxiservicecallback-verifyfile.md) | Realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó .cab archivo correspondiente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID IeAxiServiceCallback se define como \_ 1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



 

