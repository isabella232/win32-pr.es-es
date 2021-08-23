---
description: Define los datos que se usarán en la comprobación de Microsoft Authenticode de los datos de elementos.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: PST_AUTHENTICODEDATA estructura (Pstore.h)
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
ms.openlocfilehash: abf5bc69fd36e45cc715b3805f5407e821cfc7efc7f6595bcfc9eab8d762b716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690865"
---
# <a name="pst_authenticodedata-structure"></a>Estructura \_ AUTHENTICODEDATA de PST

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Define los datos que se usarán en la comprobación de Microsoft Authenticode de los datos de elementos.

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

Valor que identifica el modificador que debe comprobar una de las cadenas de llamadores.



| Valor                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**PST \_ AC \_ SINGLE \_ CALLER**</dt> <dt>0</dt> </dl>           | Solo un nivel único en la cadena de llamadas a PStore. El autor de la llamada pasa la comprobación. La imagen especificada es el llamador inmediato y es una aplicación (.exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**PST \_ AC \_ TOP \_ LEVEL \_ CALLER**</dt> <dt>1</dt> </dl> | El llamador de nivel superior debe pasar la comprobación, pero puede haber dll intermedias. La imagen especificada no es necesariamente el llamador inmediato y es una aplicación (.exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**PST \_ AC \_ IMMEDIATE \_ CALLER**</dt> <dt>2</dt> </dl>  | El llamador inmediato debe pasar la comprobación, pero no debe ser el proceso de nivel superior. La imagen especificada es el llamador inmediato y la imagen puede ser una aplicación (.exe) o un archivo DLL.<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa la entidad de certificación (CA) raíz para el certificado; use **NULL** para usar cualquier entidad de certificación disponible.

</dd> <dt>

**szIssuer**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa la ENTIDAD de certificación que emitió el certificado; use **NULL** para usar cualquier entidad de certificación disponible.

</dd> <dt>

**szPublisher**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa el publicador de software; use **NULL** para usar cualquier entidad de certificación disponible.

</dd> <dt>

**szProgramName**
</dt> <dd>

Puntero a una cadena de caracteres anchos que representa el nombre del programa; use **NULL** para usar cualquier entidad de certificación disponible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl> |



 

 
