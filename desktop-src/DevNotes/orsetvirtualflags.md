---
description: Establece marcas de virtualización en la clave del Registro abierta especificada en un subárbol del Registro sin conexión.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: Función ORSetVirtualFlags (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 56ca40b273447c8669c162b8c2dba597f2b2ce98282d40e7b482d04032a5f95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815445"
---
# <a name="orsetvirtualflags-function"></a>Función ORSetVirtualFlags

Establece marcas de virtualización en la clave del Registro abierta especificada en un subárbol del Registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro controla el comportamiento del Registro cuando se produce un error en una operación de creación o apertura en una clave de un subárbol virtualizado. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**REG \_ KEY \_ DONT \_ SILENT \_ FAIL**</dt> <dt>4</dt> </dl> | Si se establece esta marca y se produce un error en una operación Abrir en una clave para la que está habilitada la virtualización, el Registro no intenta volver a abrir la clave. Si esta marca está clara, el Registro intenta volver a abrir la clave con el acceso MÁXIMO \_ PERMITIDO.<br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**REG \_ KEY \_ DONT \_ VIRTUALIZE**</dt> <dt>2</dt> </dl>     | Si se establece esta marca y se produce un error en una operación De crear clave porque el autor de la llamada no tiene la clave KEY CREATE SUB KEY directamente en la clave primaria, el Registro produce un error en la \_ \_ operación De \_ creación. Si esta marca está clara, el Registro intenta crear la clave en el almacén virtual. El autor de la llamada debe tener el derecho \_ KEY READ en la clave primaria.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**REG \_ KEY \_ RECURSE \_ FLAG**</dt> <dt>8</dt> </dl>              | Si se establece esta marca, las marcas de virtualización del Registro se propagan desde la clave primaria. Si esta marca está clara, no se propagan las marcas de virtualización del registro.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

## <a name="remarks"></a>Comentarios

La virtualización del registro es una tecnología provisional de compatibilidad de aplicaciones que permite redirigir las operaciones de escritura de registros que tienen impacto global a ubicaciones por usuario. Este redireccionamiento es transparente para las aplicaciones que leen o escriben en el Registro.

La virtualización del registro se admite a partir de Windows Vista. Sin embargo, Microsoft pretende quitarlo de versiones futuras del sistema operativo Windows, ya que hay más aplicaciones compatibles con Windows Vista. Por lo tanto, las aplicaciones no deben depender del comportamiento de la virtualización del registro en el sistema.

La virtualización del Registro solo está habilitada para lo siguiente:

-   Procesos interactivos de 32 bits
-   Claves del software **HKEY \_ LOCAL \_ MACHINE \\**
-   Claves en las que un administrador puede escribir

Para obtener más información, vea [Registry Virtualization](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORGetVirtualFlags**](orgetvirtualflags.md)
</dt> <dt>

[Virtualización del registro](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
