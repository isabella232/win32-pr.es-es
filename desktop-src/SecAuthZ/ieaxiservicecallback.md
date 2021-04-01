---
description: Lo llama la interfaz IeAxiSystemInstaller para comprobar que se puede instalar un objeto ActiveX.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interfaz IeAxiServiceCallback
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
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913642"
---
# <a name="ieaxiservicecallback-interface"></a>Interfaz IeAxiServiceCallback

La interfaz [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) llama a la interfaz **IeAxiServiceCallback** para comprobar que se puede instalar un objeto ActiveX.

La clase [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa esta interfaz.

Esta interfaz no está declarada en un encabezado público. Las aplicaciones deben definirla. El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.

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

La interfaz **IeAxiServiceCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiServiceCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IeAxiServiceCallback** tiene estos métodos.



| Método                                                | Descripción                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**VerifyFile**](ieaxiservicecallback-verifyfile.md) | Realiza comprobaciones de seguridad en el objeto ActiveX especificado y devuelve la ubicación donde se descargó el archivo. CAB correspondiente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback se define como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



 

