---
description: La función IsValidDevmode comprueba que el contenido de una estructura DEVMODE es válido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Función IsValidDevmode (winspool. h)
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
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720729"
---
# <a name="isvaliddevmode-function"></a>IsValidDevmode función)

La función **IsValidDevmode** comprueba que el contenido de una estructura DEVMODE es válido.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevmode* \[ de\]
</dt> <dd>

Puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que se va a validar.

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

Tamaño en bytes del búfer de bytes de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True**, si la [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) es estructuralmente válida. Si se encuentran errores menores, la función los corregirá y devolverá **true**.

**False**, si [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) tiene uno o más problemas estructurales importantes. Por ejemplo, su miembro **dmSize** está mal alineado o especifica un búfer demasiado pequeño. Además, **false** si **pDevmode** es **null**.

## <a name="remarks"></a>Observaciones

No se comprueban los campos de controlador de impresora privados de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , solo los campos públicos.

Los autores de llamadas deben usar **dmSize** + **dmDriverExtra** para **DevmodeSize** solo si pueden garantizar que el tamaño del búfer de entrada sea al menos tan grande. Dado que [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) normalmente es un dato que no es de confianza, los valores que se encuentran en el búfer de entrada en los desplazamientos **dmSize** y **dmDriverExtra** también son de confianza.

Esta función se ejecuta en el contexto de la cuenta de usuario Least-Privileged (LUA).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Winspool. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **IsValidDevmodeW** (Unicode) y **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




