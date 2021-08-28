---
description: El mensaje TAPI LINE AGENTSTATUS se envía cuando cambia el estado de un agente de ACD en una línea que la aplicación \_ tiene abierta actualmente. La aplicación puede invocar lineGetAgentStatus para determinar el estado actual del agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: LINE_AGENTSTATUS mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32335e59352b773f84e8a0725c6fd97de679670cbd237f87c3e629985feb43a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959875"
---
# <a name="line_agentstatus-message"></a>Mensaje \_ DE LINE AGENTSTATUS

El mensaje TAPI **LINE \_ AGENTSTATUS** se envía cuando cambia el estado de un agente de ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar el estado actual del agente.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

El identificador de la aplicación al dispositivo de línea en el que ha cambiado el estado del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de la dirección de la línea en la que cambió el estado del agente. Un identificador de dirección está asociado permanentemente a una dirección; el identificador permanece constante en las actualizaciones del sistema operativo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado del agente que ha cambiado; puede ser una combinación de [**constantes LINEAGENTSTATUS \_**](lineagentstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam2 incluye* el bit LINEAGENTSTATUS STATE, dwParam3 indica el nuevo valor del miembro \_ **dwState** en [**LINEAGENTSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)  De lo contrario, este parámetro se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **mensaje \_ LINE AGENTSTATUS** no se envía a las aplicaciones que admiten versiones anteriores de TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




