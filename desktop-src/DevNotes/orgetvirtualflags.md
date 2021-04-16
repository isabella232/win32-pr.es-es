---
description: Recupera las marcas virtuales de la clave del registro abierta especificada en un subárbol del registro sin conexión.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Función ORGetVirtualFlags (Offreg. h)
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
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649919"
---
# <a name="orgetvirtualflags-function"></a>ORGetVirtualFlags función)

Recupera las marcas virtuales de la clave del registro abierta especificada en un subárbol del registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*pdwFlags* \[ enuncia\]
</dt> <dd>

Un puntero a una variable para recibir las marcas de virtualización establecidas para la clave. Una vez que la función devuelve un valor, este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**Reg \_ . \_Error de \_ clave \_ no silenciosa**</dt> <dt>4</dt> </dl> | Si se establece esta marca y se produce un error en una operación de apertura en una clave que tiene habilitada la virtualización, el registro no intenta volver a abrir la clave. Si esta marca está desactivada, el registro intenta volver a abrir la clave con el \_ acceso máximo permitido.<br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**Reg \_ . CLAVE \_ no \_ virtualizar**</dt> <dt>2</dt> </dl>     | Si se establece esta marca y se produce un error en una operación de creación de clave porque el autor de la llamada no tiene el \_ derecho de creación \_ de clave \_ en la clave primaria, el registro produce un error en la operación de creación. Si esta marca está desactivada, el registro intenta crear la clave en el almacén virtual. El autor de la llamada debe tener el \_ derecho de lectura de la clave en la clave primaria.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**Reg \_ . \_ \_ Marca de recursividad de clave**</dt> <dt>8</dt> </dl>              | Si se establece esta marca, las marcas de virtualización del registro se propagan desde la clave primaria. Si esta marca está desactivada, las marcas de virtualización del registro no se propagan.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

## <a name="remarks"></a>Observaciones

La virtualización del registro es una tecnología de compatibilidad de aplicaciones provisional que permite realizar operaciones de escritura en el registro que tienen un impacto global en las ubicaciones por usuario. Esta redirección es transparente para las aplicaciones que leen o escriben en el registro.

La virtualización del registro se admite a partir de Windows Vista. Sin embargo, Microsoft pretende quitarlo de versiones futuras del sistema operativo Windows a medida que se realizan más aplicaciones compatibles con Windows Vista. Por lo tanto, las aplicaciones no deben depender del comportamiento de la virtualización del registro en el sistema.

La virtualización del registro solo está habilitada para lo siguiente:

-   procesos interactivos de 32 bits
-   Claves en **el \_ \_ \\ software de máquina local HKEY**
-   Claves en las que un administrador puede escribir

Para obtener más información, consulte [virtualización del registro](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORSetVirtualFlags**](orsetvirtualflags.md)
</dt> <dt>

[Virtualización del registro](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
