---
description: Crea un perfil de usuario para un usuario especificado.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: CreateUserProfileEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987499"
---
# <a name="createuserprofileex-function"></a>CreateUserProfileEx función)

\[Esta función no está disponible en Windows Vista.\]

Crea un perfil de usuario para un usuario especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSid* \[ de\]
</dt> <dd>

Tipo: **psid**

SID del nuevo usuario.

</dd> <dt>

*lpUserName* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a un búfer que contiene el nombre de usuario del nuevo usuario.

</dd> <dt>

*lpUserHive* \[ en, opcional\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a un búfer que contiene el [subárbol del registro](../sysinfo/registry-hives.md) que se va a usar. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpProfileDir* \[ out, opcional\]
</dt> <dd>

Tipo: **LPTSTR**

Puntero a un búfer que, cuando esta función devuelve, recibe la ruta de acceso del directorio del perfil del usuario. Este parámetro puede ser **NULL**.

</dd> <dt>

*dwDirSize* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Tamaño del búfer especificado por *lpProfileDir*, en TCHARs.

</dd> <dt>

*bWin9xUpg* \[ de\]
</dt> <dd>

Tipo: **bool**

**True** si el perfil de usuario se crea como parte de una migración de perfil desde Windows 9x; en caso contrario, **false**.

Si es **true**, el perfil de usuario se configura en el directorio de perfil predeterminado, normalmente C: \\ Documents and Settings \\ *username*. Si ese directorio ya existe, se utiliza. Si no es así, se crea.

Si es **false**, se crea el directorio de perfil predeterminado si no existe. Si el directorio de perfil predeterminado ya existe, se crea un nuevo directorio para este perfil de usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Devuelve **true** si el nuevo perfil de usuario se creó correctamente; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Esta función no se declara en los encabezados del kit de desarrollo de software (SDK) y no tiene asociada ninguna biblioteca de importación. Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular a Userenv.dll. La versión ANSI de la función, a la que se hace referencia **CreateUserProfileExA** desde Userenv.dll como ordinal 153. En la versión Unicode, se hace referencia a **CreateUserProfileExW** como el ordinal 154.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/>  | Windows XP<br/>                                                                  |
| Archivo DLL<br/>                    | <dl> <dt>Userenv.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/> | **CreateUserProfileExW** (Unicode) y **CreateUserProfileExA** (ANSI)<br/>      |



 

 
