---
title: MCI_INFO_PARMS estructura (Mciapi.h)
description: La estructura \_ MCI INFO \_ PARMS contiene información para el comando INFO de MCI. \_
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- MCI_INFO_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370004"
---
# <a name="mci_info_parms-structure"></a>Estructura MCI \_ INFO \_ PARMS

La **estructura \_ MCI INFO \_ PARMS** contiene información para el [**comando INFO \_ de MCI.**](mci-info.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Búfer para la cadena de devolución.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Tamaño, en caracteres, de la cadena de devolución.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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

[**INFORMACIÓN \_ de MCI**](mci-info.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

