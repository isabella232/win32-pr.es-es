---
title: MCI_GENERIC_PARMS estructura (Mciapi.h)
description: La estructura MCI \_ GENERIC \_ PARMS contiene el identificador de la ventana que recibe mensajes de notificación. Esta estructura se usa para los mensajes de comandos de MCI que tienen listas de parámetros vacías.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- MCI_GENERIC_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246033"
---
# <a name="mci_generic_parms-structure"></a>Estructura \_ \_ parms genéricos de MCI

La **estructura MCI \_ GENERIC \_ PARMS** contiene el identificador de la ventana que recibe mensajes de notificación. Esta estructura se usa para los mensajes de comandos de MCI que tienen listas de parámetros vacías.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las **estructuras MCI \_ CLOSE \_ PARMS** y **MCI REALIZE \_ \_ PARMS** son idénticas a la estructura **\_ MCI GENERIC \_ PARMS.**

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

