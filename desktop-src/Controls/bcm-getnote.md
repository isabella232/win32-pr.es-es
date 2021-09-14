---
title: BCM_GETNOTE mensaje (Commctrl.h)
description: Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o usar la \_ macro Button GetNote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170130"
---
# <a name="bcm_getnote-message"></a>Mensaje \_ GETNOTE de BCM

Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetNote.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

DWORD **que** especifica el tamaño del búfer al que *apunta lParam*, en caracteres.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Búfer de cadena para recibir el texto. El búfer debe ser lo suficientemente grande como para dar cabida al carácter NULL final.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **TRUE.** De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Observaciones

El **mensaje \_ GETNOTE de BCM** solo funciona con botones que tienen el estilo de botón [**\_ BS COMMANDLINK**](button-styles.md) o [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) contendrá:

-   ERROR \_ NO \_ ADMITIDO, si el botón no tiene el estilo [**\_ BS DEFCOMMANDLINK**](button-styles.md) o [**\_ BS COMMANDLINK.**](button-styles.md)
-   ERROR \_ INSUFFICIENT \_ BUFFER, si el búfer *lParam* es demasiado pequeño. El *parámetro wParam* contendrá el tamaño de búfer necesario, en caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

