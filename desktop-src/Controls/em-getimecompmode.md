---
title: EM_GETIMECOMPMODE mensaje (Richedit.h)
description: Recupera el modo actual del Editor de métodos de entrada (IME) para un control de edición enriquecido.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53b9c0242872446c22034502d92af00ead7289fc68b4d5a66d79c3ef68be5eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019553"
---
# <a name="em_getimecompmode-message"></a>Mensaje \_ GETIMECOMPMODE DE EM

Recupera el modo actual del Editor de métodos de entrada (IME) para un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los siguientes valores.



| Código devuelto                                                                                     | Descripción                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_ICM NOTOPEN**</dt> </dl>     | IME no está abierto.<br/>  |
| <dl> <dt>**\_ICM LEVEL3**</dt> </dl>      | Modo en línea true.<br/> |
| <dl> <dt>**\_ICM LEVEL2**</dt> </dl>      | Nivel 2.<br/>          |
| <dl> <dt>**\_ICM LEVEL2 \_ 5**</dt> </dl>   | Nivel 2.5<br/>         |
| <dl> <dt>**\_ICM LEVEL2 \_ SUI**</dt> </dl> | Interfaz de usuario especial.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





