---
description: Crea la clave del registro especificada en un subárbol del registro sin conexión. Si la clave ya existe, la función la abre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Función ORCreateKey (Offreg. h)
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
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671489"
---
# <a name="orcreatekey-function"></a>ORCreateKey función)

Crea la clave del registro especificada en un subárbol del registro sin conexión. Si la clave ya existe, la función la abre.

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

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*lpSubKey* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nombre de una subclave que esta función abre o crea. El parámetro *lpSubKey* debe especificar una subclave de la clave identificada por el parámetro *Handle* . puede tener hasta 32 niveles de profundidad en el árbol del registro. Para obtener más información sobre los nombres de clave, vea [estructura del registro](../sysinfo/structure-of-the-registry.md).

Este parámetro no puede ser **null**.

Los nombres de clave no distinguen mayúsculas de minúsculas.

</dd> <dt>

*lpClass* \[ en, opcional\]
</dt> <dd>

La clase (tipo de objeto) de esta clave. Este parámetro se puede omitir. Este parámetro puede ser **NULL**.

</dd> <dt>

*dwOptions* \[ en, opcional\]
</dt> <dd>

Este parámetro puede ser 0 o uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**Reg \_ . OPCIÓN de \_ creación de \_ vínculo**</dt> <dt>0x00000002L</dt> </dl>    | La clave es un vínculo simbólico. La ruta de acceso de destino se asigna al valor de L "SymbolicLinkValue" de la clave. La ruta de acceso de destino debe ser una ruta de acceso absoluta del registro. Si se establece esta opción, también se debe establecer la **opción de reg \_ \_ no \_ volátil** . <br/> Si el parámetro *lpSubKey* especifica una clave existente, se debe haber creado con la **\_ opción reg \_ Create \_ Link**.<br/> Los vínculos simbólicos del registro solo deben usarse cuando sea absolutamente necesario para la compatibilidad de aplicaciones. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**Reg \_ . OPCIÓN \_ 0x00000000L no \_ volátil**</dt> <dt></dt> </dl> | La clave no es volátil; Este es el valor predeterminado. La información se almacena en un archivo y se conserva cuando se reinicia el sistema. La función [**ORSaveHive**](orsavehive.md) guarda las claves que no son volátiles.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [de \_ descriptores de seguridad](/windows/win32/api/winnt/ns-winnt-security_descriptor) que contiene un descriptor de seguridad para la nueva clave. Si *pSecurityDescriptor* es **null**, la clave obtiene un descriptor de seguridad predeterminado. Las ACL de un descriptor de seguridad predeterminado para una clave se heredan de su clave primaria directa.

</dd> <dt>

*phkResult* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un identificador de la clave abierta o creada. Utilice la función [**ORCloseKey**](orclosekey.md) para cerrar la clave después de haber terminado de usar el identificador.

</dd> <dt>

*pdwDisposition* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe uno de los siguientes valores de disposición.



| Value                                                                                                                                                                                                                                                          | Significado                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**Reg \_ . Se creó la \_ nueva \_ clave**</dt> <dt>0x00000001L</dt> </dl>             | La clave no existía y se creó.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**Reg \_ . Se abrió la \_ \_ clave existente**</dt> <dt>0x00000002L</dt> </dl> | La clave existía y se abrió simplemente sin cambiarse.<br/> |



 

Si *pdwDisposition* es **null**, no se devuelve ninguna información de disposición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

Si el parámetro *dwOptions* está establecido con **la \_ opción reg \_ Create \_ Link** , pero la **opción reg \_ \_ no \_ volatile** está clara o si el identificador que se va a devolver es un identificador de la clave raíz del subárbol, la función devuelve un parámetro de error \_ no válido \_ .

## <a name="remarks"></a>Observaciones

La clave que crea la función **ORCreateKey** no tiene valores. Una aplicación puede usar la función [**ORSetValue**](orsetvalue.md) para establecer los valores de clave.

No se puede usar la función **ORCreateKey** para crear la clave raíz en un subárbol del registro sin conexión. Utilice la función [**ORCreateHive**](orcreatehive.md) para crear la clave raíz y obtener un identificador para la clave.

El registro sin conexión no admite el guardado de claves individuales. Use la función [**ORSaveHive**](orsavehive.md) para guardar una clave y sus subclaves en un subárbol.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

[descriptor de seguridad \_](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
