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
ms.openlocfilehash: 0e2da55b721c7567b5fbc52d965cf753f896ee28fa4d76e094c7867434a69791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784315"
---
# <a name="mci_generic_parms-structure"></a>Estructura \_ \_ parms genéricos de MCI

La **estructura MCI \_ GENERIC \_ PARMS** contiene el identificador de la ventana que recibe mensajes de notificación. Esta estructura se usa para los mensajes de comandos de MCI que tienen listas de parámetros vacías.

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

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> </dl>

## <a name="remarks"></a>Comentarios

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

[**Mci**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

