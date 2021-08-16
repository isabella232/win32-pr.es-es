---
description: Actualiza los botones Atrás, Siguiente y Finalizar en el marco del asistente del cliente.
title: Método WebWizardHost.SetWizardButtons (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 36b40d0831c18a7931f3f29492dd4c7769440a76ddcec2aa33ba3e840e97950d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859128"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Método WebWizardHost.SetWizardButtons

Actualiza los **botones** Atrás, Siguiente **y** Finalizar en el marco del asistente del cliente. 

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vbEnableBack* \[ En\]
</dt> <dd>

Tipo: **booleano**

Habilita el **botón** Atrás.

</dd> <dt>

*vbEnableNext* \[ En\]
</dt> <dd>

Tipo: **booleano**

Habilita el botón **Siguiente**.

</dd> <dt>

*vbLastPage* \[ En\]
</dt> <dd>

Tipo: **booleano**

Habilita el **botón** Finalizar. Indica que esta es la última página del lado servidor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Asegúrese de implementar funciones de controlador en cada página del lado servidor para OnBack() y OnNext(), correspondientes a los botones del asistente **Atrás** y **Siguiente.** Las funciones OnBack() y OnNext() responden a **SetWizardButtons**. En el momento adecuado, la función OnNext() llama a **SetWizardButtons** con *vbLastPage* = **true**, que puede habilitar un **botón Finalizar.** OnNext() también llama a [**FinalNext**](iwebwizardhost-finalnext.md) cuando un usuario hace clic en **el botón** Finalizar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




