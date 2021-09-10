---
title: MCI_SAVE_PARMS estructura (Mciapi.h)
description: La estructura SAVE PARMS de MCI \_ contiene la información del nombre de archivo del comando SAVE de \_ \_ MCI.
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- MCI_SAVE_PARMS estructura Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370088"
---
# <a name="mci_save_parms-structure"></a>Estructura de MCI \_ SAVE \_ PARMS

La **estructura \_ SAVE \_ PARMS de MCI** contiene la información del nombre de archivo del comando SAVE [**\_ de MCI.**](mci-save.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwCallback**
</dt> <dd>

La palabra de orden bajo especifica un identificador de ventana que se usa para la marca \_ MCI NOTIFY.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nombre del archivo que se guardará.

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

[**MCI \_ SAVE**](mci-save.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

