---
description: Define los datos que se van a usar en la comprobación Authenticode de Microsoft de los datos de los elementos.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: PST_AUTHENTICODEDATA estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649813"
---
# <a name="pst_authenticodedata-structure"></a>\_Estructura AUTHENTICODEDATA de PST

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Define los datos que se van a usar en la comprobación Authenticode de Microsoft de los datos de los elementos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

**dwModifiers**
</dt> <dd>

Valor que identifica el modificador que debe comprobar una cadena de llamadores.



| Value                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**Archivo pst \_ \_Único \_ llamador AC**</dt> <dt>0</dt> </dl>           | Solo un nivel de la cadena de llamadas a PStore. El autor de la llamada pasa la comprobación de comprobación. La imagen especificada es el llamador inmediato y es una aplicación (. exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**Archivo pst \_ \_ \_ \_ Llamador de nivel superior AC**</dt> <dt>1</dt> </dl> | El autor de la llamada de nivel superior debe superar la comprobación, pero puede haber archivos dll intermedios. La imagen especificada no es necesariamente el llamador inmediato y es una aplicación (. exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**Archivo pst \_ \_ \_ Llamador inmediato AC**</dt> <dt>2</dt> </dl>  | El autor de la llamada inmediato debe superar la comprobación, pero no es necesario que sea el proceso de nivel superior. La imagen especificada es el llamador inmediato y la imagen puede ser una aplicación (. exe) o un archivo DLL.<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa la entidad de certificación (CA) raíz del certificado; Use **null** para usar cualquier CA disponible.

</dd> <dt>

**szIssuer**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa la entidad de certificación que emitió el certificado; Use **null** para usar cualquier CA disponible.

</dd> <dt>

**szPublisher**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa el editor de software; Use **null** para usar cualquier CA disponible.

</dd> <dt>

**szProgramName**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa el nombre del programa; Use **null** para usar cualquier CA disponible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
