---
description: El método RegistryValue del objeto Installer lee información sobre una clave del Registro especificada de value.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Método Installer.RegistryValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072097"
---
# <a name="installerregistryvalue-method"></a>Método Installer.RegistryValue

El **método RegistryValue** del [**objeto Installer**](installer-object.md) lee información sobre una clave del Registro especificada de value. Si la clave o el valor especificado no existen, el método devuelve un error de 9, "Subscript out of Range".

## <a name="syntax"></a>Sintaxis


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*root* 
</dt> <dd>

En Windows NT 4.0, la raíz del Registro es una clave raíz numérica o un nombre de equipo como una cadena. Los nombres de equipo siempre son cadenas. En Windows 95, Windows 98 o Windows me, la raíz del Registro es solo una clave raíz numérica. Solo puede acceder a HKLM en una máquina remota.



| Root                                                                                                                                                                                   | Significado      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**RAÍZ DE CLASES HKEY \_ \_**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**USUARIO ACTUAL DE HKEY \_ \_**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**HKEY \_ LOCAL \_ MACHINE**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**USUARIOS DE \_ HKEY**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**HKEY \_ PERFORMANCE \_ DATA**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**CONFIGURACIÓN ACTUAL DE HKEY \_ \_**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**HKEY \_ DYN \_ DATA**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*key* 
</dt> <dd>

Cadena que contiene la ruta de acceso de clave completa de la raíz.

</dd> <dt>

*value* 
</dt> <dd>

Este parámetro opcional designa el valor asociado que se va a devolver para la clave especificada. El valor es uno de los valores que se muestran en la tabla siguiente.



| Value                                                                                                                                                                                                    | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Falta o está en blanco**</dt> </dl> | Devuelve un valor booleano que designa si la clave existe.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**String**</dt> </dl>                                         | Devuelve los datos asociados al valor con nombre; se produce un error si el nombre del valor no existe.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Entero positivo**</dt> </dl> | Devuelve el nombre del valor enumerado basado en 1, que está vacío si no existe. Esta opción usa la [**función RegEnumValue.**](/windows/win32/api/winreg/nf-winreg-regenumvaluea)<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Entero negativo**</dt> </dl> | Devuelve el nombre de la subclave enumerada basada en 1, que está vacía si no existe. Esta opción usa la [**función RegEnumKey.**](/windows/win32/api/winreg/nf-winreg-regenumkeya)<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**Número entero cero**</dt> </dl>                 | Devuelve el nombre de clase de cadena para la clave designada.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Cadena vacía " "**</dt> </dl> | Devuelve el valor predeterminado de la clave del Registro.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
