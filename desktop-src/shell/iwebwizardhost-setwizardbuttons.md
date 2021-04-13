---
description: Actualiza los botones atrás, siguiente y finalizar en el marco del asistente del cliente.
title: Método WebWizardHost. SetWizardButtons (Shldisp. h)
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
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985786"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>WebWizardHost. SetWizardButtons, método

Actualiza los botones **atrás**, **siguiente** y **Finalizar** en el marco del asistente del cliente.

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

*vbEnableBack* \[ de\]
</dt> <dd>

Tipo: **booleano**

Habilita el botón **atrás** .

</dd> <dt>

*vbEnableNext* \[ de\]
</dt> <dd>

Tipo: **booleano**

Habilita el botón **Siguiente**.

</dd> <dt>

*vbLastPage* \[ de\]
</dt> <dd>

Tipo: **booleano**

Habilita el botón **Finalizar** . Indica que se trata de la última página del servidor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Asegúrese de implementar las funciones de controlador en cada página del servidor para la función alback () y en la siguiente (), correspondientes a los botones del asistente **atrás** y **siguiente**. Las funciones alback () y alnext () responden a **SetWizardButtons**. En el momento adecuado, la función Next () llama a **SetWizardButtons** con *vbLastPage* = **true**, que puede habilitar un botón **Finalizar** . El siguiente () también llama a [**FinalNext**](iwebwizardhost-finalnext.md) cuando un usuario hace clic en el botón **Finalizar** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




