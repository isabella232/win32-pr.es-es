---
description: La función IsValidDevmode comprueba que el contenido de una estructura DEVMODE es válido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Función IsValidDevmode (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4c3a5cd33a6a5584ea9373df22df51a09e3e763d284a0f979f0b24e3651dc3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100533"
---
# <a name="isvaliddevmode-function"></a>Función IsValidDevmode

La **función IsValidDevmode** comprueba que el contenido de una estructura DEVMODE es válido.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevmode* \[ En\]
</dt> <dd>

Puntero al [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que se validará.

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

Tamaño en bytes del búfer de bytes de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE**, si [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) es estructuralmente válido. Si se encuentran errores menores, la función los corregirá y devolverá **TRUE**.

**FALSE**, si [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) tiene uno o varios problemas estructurales importantes. Por ejemplo, su **miembro dmSize** está mal alineado o especifica un búfer demasiado pequeño. Además, **FALSE si** **pDevmode** es **NULL.**

## <a name="remarks"></a>Comentarios

No se comprueba ningún campo de controlador de impresora privado [**de DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) solo los campos públicos.

Los llamadores deben usar **dmSize** + **dmDriverExtra** para **DevmodeSize** solo si pueden garantizar que el tamaño del búfer de entrada sea al menos ese grande. Dado que [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) no suele ser datos de confianza, los valores que se encuentran en el búfer de entrada en los desplazamientos **dmSize** y **dmDriverExtra** tampoco son de confianza.

Esta función es ejecutable en Least-Privileged de cuenta de usuario (LUA).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Winspool.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **IsValidDevmodeW** (Unicode) e **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




