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
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842626"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Método WebWizardHost.SetWizardButtons

Actualiza los **botones** **Atrás,** Siguiente **y** Finalizar en el marco del asistente del cliente.

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

## <a name="remarks"></a>Observaciones

Asegúrese de implementar funciones de controlador en cada página del lado servidor para OnBack() y OnNext(), correspondientes a los botones del asistente **Atrás** y **Siguiente.** Las funciones OnBack() y OnNext() responden a **SetWizardButtons**. En el momento adecuado, la función OnNext() llama a **SetWizardButtons** con *vbLastPage* true , que = puede habilitar un **botón Finalizar.** OnNext() también llama a [**FinalNext**](iwebwizardhost-finalnext.md) cuando un usuario hace clic en **el botón** Finalizar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




