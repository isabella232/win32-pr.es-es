---
title: Mensaje EM_GETIMECOMPMODE (RichEdit. h)
description: Recupera el modo del editor de métodos de entrada (IME) actual para un control Rich Edit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE controles de mensajes de Windows
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
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491806"
---
# <a name="em_getimecompmode-message"></a>\_Mensaje GETIMECOMPMODE em

Recupera el modo del editor de métodos de entrada (IME) actual para un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los valores siguientes.



| Código devuelto                                                                                     | Descripción                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_NOTOPEN ICM**</dt> </dl>     | El IME no está abierto.<br/>  |
| <dl> <dt>**\_Level3 ICM**</dt> </dl>      | Verdadero modo insertado.<br/> |
| <dl> <dt>**\_LEVEL2 ICM**</dt> </dl>      | Nivel 2.<br/>          |
| <dl> <dt>**ICM \_ LEVEL2 \_ 5**</dt> </dl>   | Nivel 2,5<br/>         |
| <dl> <dt>**LEVEL2 de ICM \_ \_**</dt> </dl> | Interfaz de usuario especial.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





