---
description: Contiene información que identifica el adaptador.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9 estructura (D3D9Types.h)
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
ms.openlocfilehash: 843dff64de7ad4b97b2719f469bb8fb13813f06b8045d7de1b9f5ec4215a76ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989245"
---
# <a name="d3dadapter_identifier9-structure"></a>Estructura D3DADAPTER \_ IDENTIFIER9

Contiene información que identifica el adaptador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
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

Tipo: **char**

</dd> <dd>

Se usa para la presentación al usuario. Esto no debe usarse para identificar controladores concretos, ya que muchas cadenas diferentes podrían estar asociadas al mismo dispositivo y controlador de proveedores diferentes.

</dd> <dt>

**Descripción**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Se usa para la presentación al usuario.

</dd> <dt>

**DeviceName**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Nombre del dispositivo para GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Tipo: **[ **ENTERO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identifique la versión del controlador Direct3D. Es legal realizar comparaciones menores y mayores que en el valor entero de 64 bits con signo. Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos. En su lugar, debe usar DeviceIdentifier. Vea la sección Comentarios.

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifique la versión del controlador Direct3D. Es válido realizar comparaciones < y > en el valor entero de 64 bits con signo. Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos. En su lugar, debe usar DeviceIdentifier. Vea la sección Comentarios.

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifique la versión del controlador Direct3D. Es válido realizar comparaciones < y > en el valor entero de 64 bits con signo. Sin embargo, tenga cuidado si usa este elemento para identificar controladores problemáticos. En su lugar, debe usar DeviceIdentifier. Vea la sección Comentarios.

</dd> <dt>

**VendorId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar al fabricante. El valor puede ser cero si es desconocido.

</dd> <dt>

**DeviceId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar el tipo de conjunto de chip. El valor puede ser cero si es desconocido.

</dd> <dt>

**SubSysId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar el subsistema, normalmente la placa determinada. El valor puede ser cero si es desconocido.

</dd> <dt>

**Revisión**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se puede usar para ayudar a identificar un conjunto de chips determinado. Consulte este miembro para identificar el nivel de revisión del conjunto de chips. El valor puede ser cero si es desconocido.

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

Tipo: **[ **GUID**](guid.md)**

</dd> <dd>

Se puede consultar para comprobar los cambios en el controlador y el conjunto de chips. Este GUID es un identificador único para el par de controladores y conjunto de chips. Consulte este miembro para realizar un seguimiento de los cambios en el controlador y el conjunto de chips con el fin de generar un nuevo perfil para el subsistema de gráficos. DeviceIdentifier también se puede usar para identificar controladores problemáticos concretos.

</dd> <dt>

**WHQLLevel**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Se usa para determinar el Windows de validación de Hardware Quality Labs (WHQL) para este par de controladores y dispositivos. DWORD es una estructura de fecha empaquetada que define la fecha de lanzamiento de la prueba WHQL más reciente superada por el controlador. Es válido realizar operaciones < y > en este valor. A continuación se muestra el formato de fecha.



| Bits  |  Descripción                                             |
|-------|-----------------------------------------------|
| 31-16 | El año, un número decimal de 1999 hacia arriba. |
| 15-8  | El mes, un número decimal de 1 a 12.     |
| 7-0   | El día, un número decimal de 1 a 31.       |



 

También se usan los siguientes valores.



| Value    |  Descripción                                                     |
|-----|-------------------------------------------------------|
| 0   | No certificado.                                        |
| 1   | WHQL validado, pero no hay información de fecha disponible. |



 

Diferencias entre Direct3D 9 y Direct3D 9Ex:

Para Direct3D9Ex que se ejecuta en Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 (o más sistema operativo actual), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) devuelve 1 para el nivel WHQL sin comprobar el estado del controlador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En el ejemplo de pseudocódigo siguiente se muestra el formato de versión codificado en los miembros DriverVersion, DriverVersionLowPart y DriverVersionHighPart.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Consulte Platform SDK para obtener más información sobre la macro HIWORD, la macro LOWORD y la estructura LARGE \_ INTEGER.

MAX \_ DEVICE IDENTIFIER STRING es una constante con la siguiente \_ \_ definición.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



Los miembros VendorId, DeviceId, SubSysId y Revision se pueden usar conjuntamente para identificar conjuntos de chips concretos. Sin embargo, use estos miembros con precaución.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
