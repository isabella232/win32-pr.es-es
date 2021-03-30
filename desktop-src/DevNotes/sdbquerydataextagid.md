---
description: Recupera datos de las entradas especificadas que pertenecen a una entrada EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID función)
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
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423207"
---
# <a name="sdbquerydataextagid-function"></a>SdbQueryDataExTagID función)

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

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tiExe* \[ de\]
</dt> <dd>

[**TAGID**](tagid.md) de la entrada exe.

</dd> <dt>

*lpszDataName* \[ en, opcional\]
</dt> <dd>

Nombre de la entrada de datos que se va a recuperar. Para especificar varias entradas, separe los nombres con el carácter de barra diagonal inversa (" \\ "). Si este parámetro es **null**, la función intenta devolver todas las entradas de datos.

</dd> <dt>

*lpdwDataType* \[ out, opcional\]
</dt> <dd>

El tipo de datos de las entradas devueltas. Este parámetro puede ser uno de los siguientes valores:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**\_binario de reg**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**\_valor DWORD reg**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ multi \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ ninguno**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**QWord de REG \_**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**Registro \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ enuncia\]
</dt> <dd>

Búfer que recibe los datos. Si el búfer no es lo suficientemente grande como para contener los datos, se produce un error en la función y se devuelve un **error de \_ \_ búfer insuficiente**.

</dd> <dt>

*lpcbBufferSize* \[ in, out, opcional\]
</dt> <dd>

Tamaño del búfer de *lpBuffer* , en bytes.

</dd> <dt>

*ptiData* \[ enuncia\]
</dt> <dd>

[**TAGID**](tagid.md) de la entrada de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los valores siguientes.



| Código devuelto                                                                                                    | Descripción                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>       | Uno o varios parámetros de entrada no son correctos.<br/>                  |
| <dl> <dt>**ERROR \_ de \_ base de BD interna \_ dañado**</dt> </dl> | No se encontraron entradas de datos para la entrada EXE.<br/>               |
| <dl> <dt>**ERROR \_ de \_ búfer insuficiente**</dt> </dl>     | El búfer no es suficientemente grande para contener las entradas de datos.<br/> |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl>      | Error de asignación de memoria.<br/>                               |
| <dl> <dt>**\_no \_ se encontró el error**</dt> </dl>               | No se encontró una entrada de datos con el nombre *lpszDataName* .<br/>    |
| <dl> <dt>**ERROR \_ correcto**</dt> </dl>                  | La función se completó correctamente.<br/>                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




