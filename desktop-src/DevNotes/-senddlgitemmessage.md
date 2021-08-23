---
description: Envía un mensaje al control especificado en un cuadro de diálogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 3a1c17ab1ad303ce95755140ebe7f264b976471c7ecfa507f2152ec9e0ad221c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538845"
---
# <a name="_senddlgitemmessage-function"></a>\_Función SendDlgItemMessage

\[Esta función es un contenedor sobre la **función SendDlgItemMessage.** Esta función puede modificarse o no estar disponible en el futuro. Las aplicaciones deben **llamar directamente a SendDlgItemMessage.**\]

Envía un mensaje al control especificado en un cuadro de diálogo. Vea [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).

## <a name="syntax"></a>Sintaxis


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
