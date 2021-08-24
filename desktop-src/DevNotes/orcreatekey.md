---
description: Crea la clave del Registro especificada en un subárbol del Registro sin conexión. Si la clave ya existe, la función la abre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Función ORCreateKey (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b7ea5a365a9c5bdcb478ce47443a713ed5bc091666b54de880dc478708e4c36c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749695"
---
# <a name="orcreatekey-function"></a>Función ORCreateKey

Crea la clave del Registro especificada en un subárbol del Registro sin conexión. Si la clave ya existe, la función la abre.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*lpSubKey* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nombre de una subclave que esta función abre o crea. El *parámetro lpSubKey* debe especificar una subclave de la clave identificada por el *parámetro Handle;* puede tener hasta 32 niveles de profundidad en el árbol del Registro. Para obtener más información sobre los nombres de clave, vea [Estructura del Registro](../sysinfo/structure-of-the-registry.md).

Este parámetro no puede ser **NULL.**

Los nombres de clave no distinguen mayúsculas de minúsculas.

</dd> <dt>

*lpClass* \[ in, opcional\]
</dt> <dd>

Clase (tipo de objeto) de esta clave. Este parámetro puede omitirse. Este parámetro puede ser **NULL**.

</dd> <dt>

*dwOptions* \[ in, opcional\]
</dt> <dd>

Este parámetro puede ser 0 o uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**REG \_ OPCIÓN \_ CREATE \_ LINK**</dt> <dt>0x00000002L</dt> </dl>    | La clave es un vínculo simbólico. La ruta de acceso de destino se asigna al valor L"SymbolicLinkValue" de la clave. La ruta de acceso de destino debe ser una ruta de acceso del Registro absoluta. Si se establece esta opción, también se debe establecer **REG \_ OPTION NON \_ \_ VOLATILE.** <br/> Si el *parámetro lpSubKey* especifica una clave existente, se debe haber creado con **REG OPTION CREATE \_ \_ \_ LINK.**<br/> Los vínculos simbólicos del Registro solo se deben usar cuando sea absolutamente necesario para la compatibilidad de aplicaciones. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**REG \_ OPCIÓN \_ NO \_ VOLÁTIL**</dt> <dt>0x00000000L</dt> </dl> | La clave no es volátil; este es el valor predeterminado. La información se almacena en un archivo y se conserva cuando se reinicia el sistema. La [**función ORSaveHive**](orsavehive.md) guarda claves que no son volátiles.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ in, opcional\]
</dt> <dd>

Puntero a una estructura [ \_ DE DESCRIPTOR DE SEGURIDAD](/windows/win32/api/winnt/ns-winnt-security_descriptor) que contiene un descriptor de seguridad para la nueva clave. Si *pSecurityDescriptor* es **NULL,** la clave obtiene un descriptor de seguridad predeterminado. Las ACL de un descriptor de seguridad predeterminado para una clave se heredan de su clave primaria directa.

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un identificador para la clave abierta o creada. Use la [**función ORCloseKey**](orclosekey.md) para cerrar la clave una vez que haya terminado de usar el identificador.

</dd> <dt>

*pdwDisposition* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe uno de los siguientes valores de disposición.



| Value                                                                                                                                                                                                                                                          | Significado                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**REG \_ CREATED \_ NEW \_ KEY**</dt> <dt>0x00000001L</dt> </dl>             | La clave no existía y se creó.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**REG \_ OPENED \_ EXISTING \_ KEY**</dt> <dt>0x00000002L</dt> </dl> | La clave existía y simplemente se abrió sin cambiarse.<br/> |



 

Si *pdwDisposition* es **NULL,** no se devuelve información de disposición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

Si el *parámetro dwOptions* se establece con **REG OPTION CREATE \_ \_ \_ LINK** pero **REG OPTION NON \_ \_ \_ VOLATILE** está claro, o si el identificador que se va a devolver sería un identificador para la clave raíz del subárbol, la función devuelve ERROR \_ INVALID \_ PARAMETER.

## <a name="remarks"></a>Comentarios

La clave que crea **la función ORCreateKey** no tiene valores. Una aplicación puede usar la [**función ORSetValue**](orsetvalue.md) para establecer valores de clave.

La **función ORCreateKey** no se puede usar para crear la clave raíz en un subárbol del Registro sin conexión. Use la [**función ORCreateHive**](orcreatehive.md) para crear la clave raíz y obtener un identificador para la clave.

El registro sin conexión no admite el guardado de claves individuales. Use la [**función ORSaveHive**](orsavehive.md) para guardar una clave y sus subclaves en un subárbol.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[DESCRIPTOR \_ DE SEGURIDAD](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
