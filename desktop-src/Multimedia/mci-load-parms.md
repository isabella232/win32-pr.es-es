---
title: Estructura de MCI_LOAD_PARMS (mmsystem. h)
description: La \_ estructura de parms de carga de MCI \_ contiene el nombre de archivo que se va a cargar para el \_ comando MCI Load.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- Estructura de MCI_LOAD_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803361"
---
# <a name="mci_load_parms-structure"></a>\_Estructura parms de carga de MCI \_

La estructura de **\_ \_ parms de carga de MCI** contiene el nombre de archivo que se va a cargar para el comando [**MCI \_ Load**](mci-load.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .

</dd> <dt>

**lpfilename**
</dt> <dd>

Nombre del archivo que se va a cargar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estructuras de MCI**](mci-structures.md)
</dt> <dt>

[**carga de MCI \_**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

