---
description: Contiene información que identifica el adaptador.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9 estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33aba75cafff5f9e69a74d5570f98455a9853289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717673"
---
# <a name="d3dadapter_identifier9-structure"></a>D3DADAPTER \_ estructura IDENTIFIER9

Contiene información que identifica el adaptador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Controlador**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

Se usa para la presentación al usuario. No debe usarse para identificar determinados controladores, ya que muchas cadenas diferentes podrían estar asociadas con el mismo dispositivo y controlador de distintos proveedores.

</dd> <dt>

**Descripción**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

Se usa para la presentación al usuario.

</dd> <dt>

**DeviceName**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

Nombre del dispositivo para GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Tipo: **[ **\_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identifique la versión del controlador Direct3D. Es válido realizar comparaciones menores que y mayores que en el valor entero con signo de 64 bits. Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos. En su lugar, debe usar DeviceIdentifier. Vea la sección Comentarios.

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifique la versión del controlador Direct3D. Es legal realizar comparaciones de < y > en el valor entero con signo de 64 bits. Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos. En su lugar, debe usar DeviceIdentifier. Vea la sección Comentarios.

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifique la versión del controlador Direct3D. Es legal realizar comparaciones de < y > en el valor entero con signo de 64 bits. Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos. En su lugar, debe usar DeviceIdentifier. Vea la sección Comentarios.

</dd> <dt>

**VendorId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar al fabricante. El valor puede ser cero si se desconoce.

</dd> <dt>

**DeviceId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar el tipo de conjunto de chips. El valor puede ser cero si se desconoce.

</dd> <dt>

**SubSysId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar el subsistema, normalmente el panel en cuestión. El valor puede ser cero si se desconoce.

</dd> <dt>

**Revisión**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar el nivel de revisión del conjunto de chips. El valor puede ser cero si se desconoce.

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

Tipo: **[ **GUID**](guid.md)**

</dd> <dd>

Se puede consultar para comprobar los cambios en el controlador y en el conjunto de chips. Este GUID es un identificador único para el par de controladores y conjuntos de chips. Consulte este miembro para realizar el seguimiento de los cambios en el controlador y en el conjunto de chips con el fin de generar un nuevo perfil para el subsistema de gráficos. DeviceIdentifier también se puede usar para identificar determinados controladores problemáticos.

</dd> <dt>

**WHQLLevel**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se usa para determinar el nivel de validación de los laboratorios de calidad de hardware de Windows (WHQL) para este par de controlador y dispositivo. El valor DWORD es una estructura de fecha empaquetada que define la fecha de la versión de la prueba de WHQL más reciente pasada por el controlador. Es válido realizar operaciones de < y > en este valor. A continuación se muestra el formato de fecha.



|       |                                               |
|-------|-----------------------------------------------|
| Bits  |                                               |
| 31-16 | El año, un número decimal de 1999 en adelante. |
| 15-8  | El mes, un número decimal comprendido entre 1 y 12.     |
| 7-0   | El día, un número decimal comprendido entre 1 y 31.       |



 

También se utilizan los valores siguientes.



|     |                                                       |
|-----|-------------------------------------------------------|
| 0   | No certificado.                                        |
| 1   | WHQL validado, pero no hay información de fecha disponible. |



 

Diferencias entre Direct3D 9 y Direct3D 9Ex:

Para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual), [**IDirect3D9:: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) devuelve 1 para el nivel de WHQL sin comprobar el estado del controlador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el siguiente ejemplo de pseudocódigo se muestra el formato de versión codificado en los miembros DriverVersion, DriverVersionLowPart y DriverVersionHighPart.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Vea el SDK de la plataforma para obtener más información sobre la macro HIWORD, la macro LOWORD y la \_ estructura de enteros grandes.

MAX \_ Device \_ Identifier \_ String es una constante con la siguiente definición.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



Los miembros VendorId, DeviceId, SubSysId y revision se pueden usar conjuntamente para identificar determinados conjuntos de chips. Sin embargo, utilice estos miembros con precaución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
