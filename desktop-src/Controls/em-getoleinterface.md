---
title: Mensaje EM_GETOLEINTERFACE (RichEdit. h)
description: Recupera un objeto IRichEditOle que un cliente puede utilizar para tener acceso a la funcionalidad del modelo de objetos componentes (COM) de un control Rich Edit.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150665"
---
# <a name="em_getoleinterface-message"></a>\_Mensaje GETOLEINTERFACE em

Recupera un objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) que un cliente puede utilizar para tener acceso a la funcionalidad del modelo de objetos componentes (com) de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un puntero que recibe el objeto [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) . El control llama al método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para el objeto antes de devolver, por lo que la aplicación que realiza la llamada debe llamar al método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando se realiza con el objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

