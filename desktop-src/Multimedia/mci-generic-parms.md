---
title: MCI_GENERIC_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura parms genérica de MCI contiene el identificador de la ventana que recibe los mensajes de notificación. Esta estructura se usa para los mensajes de comandos MCI que tienen listas de parámetros vacías.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- Estructura de MCI_GENERIC_PARMS de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490121"
---
# <a name="mci_generic_parms-structure"></a>\_Estructura parms genérica de MCI \_

La **estructura \_ \_ parms genérica de MCI** contiene el identificador de la ventana que recibe los mensajes de notificación. Esta estructura se usa para los mensajes de comandos MCI que tienen listas de parámetros vacías.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las estructuras **MCI \_ Close \_ parms** y **MCI \_ observan \_ parms** son idénticas a la estructura **\_ \_ parms de MCI genérica** .

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

