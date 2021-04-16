---
description: Escribe datos binarios en la base de datos especificada.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: SdbWriteBinaryTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538644"
---
# <a name="sdbwritebinarytag-function"></a>SdbWriteBinaryTag función)

Escribe datos binarios en la base de datos especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tTag* \[ de\]
</dt> <dd>

ETIQUETA de la entrada. Esta etiqueta debe ser de tipo **etiqueta \_ \_ binaria**.

</dd> <dt>

*pBuffer* \[ de\]
</dt> <dd>

Búfer que contiene los datos. Este parámetro no puede ser **null**.

</dd> <dt>

*dwSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *pBuffer* , en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




