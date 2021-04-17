---
title: Mensaje de PSM_PAGETOINDEX (Prsht. h)
description: Toma el identificador HPROPSHEETPAGE de la página de la hoja de propiedades y devuelve su índice basado en cero. Puede enviar este mensaje explícitamente o utilizar la \_ macro PropSheet PageToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- PSM_PAGETOINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658228"
---
# <a name="psm_pagetoindex-message"></a>Mensaje de PSM \_ PAGETOINDEX

Toma el identificador HPROPSHEETPAGE de la página de la hoja de propiedades y devuelve su índice basado en cero. Puede enviar este mensaje explícitamente o utilizar la macro [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de HPROPSHEETPAGE de la página de la hoja de propiedades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero de la página de la hoja de propiedades especificada por *lParam* si se realiza correctamente. De lo contrario, devuelve -1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





