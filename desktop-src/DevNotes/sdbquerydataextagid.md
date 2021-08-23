---
description: Recupera datos de las entradas especificadas que pertenecen a una entrada EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: Función SdbQueryDataExTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 19477385fb70f65c560d1a13d479fc4c2ce1853220aff6ac32a75f3634a40d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815385"
---
# <a name="sdbquerydataextagid-function"></a>Función SdbQueryDataExTagID

Recupera datos de las entradas especificadas que pertenecen a una entrada EXE.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tiExe* \[ En\]
</dt> <dd>

TAGID [**de**](tagid.md) la entrada EXE.

</dd> <dt>

*lpszDataName* \[ in, opcional\]
</dt> <dd>

Nombre de la entrada de datos que se va a recuperar. Para especificar varias entradas, separe los nombres con el carácter de barra diagonal inversa (" \\ "). Si este parámetro es **NULL,** la función intenta devolver todas las entradas de datos.

</dd> <dt>

*lpdwDataType* \[ out, opcional\]
</dt> <dd>

Tipo de datos de las entradas devueltas. Este parámetro puede ser uno de los siguientes valores:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**REG \_ BINARY**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ MULTI \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ NONE**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Búfer que recibe los datos. Si el búfer no es lo suficientemente grande como para contener los datos, se produce un error en la función y devuelve **ERROR \_ INSUFFICIENT \_ BUFFER**.

</dd> <dt>

*lpcbBufferSize* \[ in, out, optional\]
</dt> <dd>

Tamaño del búfer *lpBuffer,* en bytes.

</dd> <dt>

*ptiData* \[ out\]
</dt> <dd>

TAGID [**de**](tagid.md) la entrada de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los valores siguientes.



| Código devuelto                                                                                                    | Descripción                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>       | Uno o varios parámetros de entrada son incorrectos.<br/>                  |
| <dl> <dt>**ERROR DAÑOS \_ EN LA BASE DE DATOS \_ \_ INTERNA**</dt> </dl> | No se encontraron entradas de datos para la entrada EXE.<br/>               |
| <dl> <dt>**ERROR \_ BÚFER \_ INSUFICIENTE**</dt> </dl>     | El búfer no es lo suficientemente grande como para contener las entradas de datos.<br/> |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl>      | Error en la asignación de memoria.<br/>                               |
| <dl> <dt>**ERROR \_ NO \_ ENCONTRADO**</dt> </dl>               | No se encontró una entrada de datos con el nombre *lpszDataName.*<br/>    |
| <dl> <dt>**ERROR \_ CORRECTO**</dt> </dl>                  | La función se completó correctamente.<br/>                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




