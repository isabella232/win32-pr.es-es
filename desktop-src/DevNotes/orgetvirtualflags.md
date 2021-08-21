---
description: Recupera las marcas virtuales de la clave del Registro abierta especificada en un subárbol del Registro sin conexión.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Función ORGetVirtualFlags (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 8f0e44c388b576bb514ed86f2a537cefaf1a4f0984e3e5beb1b466e88c5b82c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076059"
---
# <a name="orgetvirtualflags-function"></a>Función ORGetVirtualFlags

Recupera las marcas virtuales de la clave del Registro abierta especificada en un subárbol del Registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Puntero a una variable para recibir las marcas de virtualización establecidas para la clave. Una vez que la función vuelve, este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**REG \_ KEY \_ DONT \_ SILENT \_ FAIL**</dt> <dt>4</dt> </dl> | Si se establece esta marca y se produce un error en una operación De apertura en una clave que tiene habilitada la virtualización, el Registro no intenta volver a abrir la clave. Si esta marca está clara, el Registro intenta volver a abrir la clave con el acceso MÁXIMO \_ PERMITIDO.<br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**REG \_ KEY \_ DONT \_ VIRTUALIZE**</dt> <dt>2</dt> </dl>     | Si se establece esta marca y se produce un error en una operación De crear clave porque el autor de la llamada no tiene la clave KEY CREATE SUB KEY justo en la clave primaria, el Registro produce un error en la \_ \_ operación de \_ creación. Si esta marca está clara, el Registro intenta crear la clave en el almacén virtual. El autor de la llamada debe tener el derecho \_ KEY READ en la clave primaria.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**REG \_ MARCA \_ RECURSE \_ CLAVE**</dt> <dt>8</dt> </dl>              | Si se establece esta marca, las marcas de virtualización del Registro se propagan desde la clave primaria. Si esta marca está clara, las marcas de virtualización del registro no se propagan.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

## <a name="remarks"></a>Comentarios

La virtualización del registro es una tecnología provisional de compatibilidad de aplicaciones que permite redirigir las operaciones de escritura del registro que tienen un impacto global a ubicaciones por usuario. Este redireccionamiento es transparente para las aplicaciones que leen o escriben en el Registro.

La virtualización del registro se admite a partir de Windows Vista. Sin embargo, Microsoft pretende quitarlo de versiones futuras del sistema operativo Windows, ya que hay más aplicaciones compatibles con Windows Vista. Por lo tanto, las aplicaciones no deben depender del comportamiento de la virtualización del registro en el sistema.

La virtualización del Registro solo está habilitada para lo siguiente:

-   Procesos interactivos de 32 bits
-   Claves en **HKEY \_ LOCAL MACHINE \_ \\ Software**
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

[**ORSetVirtualFlags**](orsetvirtualflags.md)
</dt> <dt>

[Virtualización del registro](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
