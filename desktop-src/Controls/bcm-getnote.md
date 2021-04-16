---
title: Mensaje de BCM_GETNOTE (commctrl. h)
description: Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetNote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658214"
---
# <a name="bcm_getnote-message"></a>\_Mensaje GETNOTE de BCM

Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

**DWORD** que especifica el tamaño del búfer señalado por *lParam*, en caracteres.

</dd> <dt>

*lParam* \[ enuncia\]
</dt> <dd>

Búfer de cadena para recibir el texto. El búfer debe ser lo suficientemente grande como para dar cabida al carácter nulo de terminación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **true**. En caso contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

El **mensaje \_ GETNOTE de BCM** solo funciona con los botones que tienen el estilo de botón [**BS \_ COMMANDLINK**](button-styles.md) o [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) contendrá:

-   ERROR \_ no \_ compatible, si el botón no tiene el estilo [**BS \_ DEFCOMMANDLINK**](button-styles.md) o [**BS \_ COMMANDLINK**](button-styles.md) .
-   ERROR \_ de \_ búfer insuficiente, si el búfer *lParam* es demasiado pequeño. El parámetro *wParam* contendrá el tamaño de búfer necesario, en caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

