---
description: Obtiene el nivel de una regla de identificación hash que coincide con el hash especificado.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496487"
---
# <a name="saferisearchmatchinghashrules-function"></a>SaferiSearchMatchingHashRules función)

Obtiene el nivel de una regla de identificación hash que coincide con el hash especificado.

Esta función no tiene asociada ninguna biblioteca de importación y no está declarada en un encabezado público. Debe definir un puntero a función con la firma de esta función, y debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Advapi32.dll.

Se recomienda usar la función [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) para evaluar las directivas de restricción de software.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HashAlgorithm* \[ en, opcional\]
</dt> <dd>

Identificador del algoritmo utilizado para crear el hash.

</dd> <dt>

*pHashBytes* \[ de\]
</dt> <dd>

Puntero a una matriz de bytes que contiene el hash.

</dd> <dt>

*dwHashSize* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la matriz *pHashBytes* .

</dd> <dt>

*dwOriginalImageSize* \[ en, opcional\]
</dt> <dd>

Tamaño, en bytes, de la imagen original a partir de la cual se calculó el hash.

</dd> <dt>

*pdwFoundLevel* \[ enuncia\]
</dt> <dd>

Puntero al identificador de nivel para la regla de identificación hash coincidente.

</dd> <dt>

*pdwSaferFlags* 
</dt> <dd>

Reservado. Establezca este valor en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si la función se realiza correctamente; en caso contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
