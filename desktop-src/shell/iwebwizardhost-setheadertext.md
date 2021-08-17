---
description: Establece el título y el subtítulo que aparecen en el encabezado del asistente. En general, el cliente mostrará el encabezado encima del CÓDIGO HTML y debajo de la barra de título.
title: Método WebWizardHost.SetHeaderText (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d97bb8ac1823801257f0ad9f2a737a78bafbf6d724c0f56f3ff0607e498a61bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859199"
---
# <a name="webwizardhostsetheadertext-method"></a>Método WebWizardHost.SetHeaderText

Establece el título y el subtítulo que aparecen en el encabezado del asistente. En general, el cliente mostrará el encabezado encima del CÓDIGO HTML y debajo de la barra de título.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrHeaderTitle* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena que contiene el título.

</dd> <dt>

*bstrHeaderSubtitle* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena que contiene el subtítulo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 
