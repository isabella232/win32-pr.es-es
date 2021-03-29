---
description: Implementa las interfaces IAxiService y IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Objeto CIeAxiInstallerService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001221"
---
# <a name="cieaxiinstallerservice-object"></a>Objeto CIeAxiInstallerService

El objeto **CIeAxiInstallerService** implementa las interfaces [**IAxiService**](ieaxiservice.md) y [**IeAxiServiceCallback**](ieaxiservicecallback.md) .

Este objeto no se declara en un encabezado público. Las aplicaciones deben definirla. El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe este objeto, incluido su CLSID.

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAxiService**](ieaxiservice.md)
</dt> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

 




