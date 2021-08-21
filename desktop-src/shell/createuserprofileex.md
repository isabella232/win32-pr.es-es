---
description: Crea un perfil de usuario para un usuario especificado.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: Función CreateUserProfileEx
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
ms.openlocfilehash: e6a507c508d508bc11946fe4c68d79e459135956e0a0539dd4c9a0fee2f04a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050822"
---
# <a name="createuserprofileex-function"></a>Función CreateUserProfileEx

\[Esta función no está disponible a Windows Vista.\]

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

*pSid* \[ En\]
</dt> <dd>

Tipo: **PSID**

SID del nuevo usuario.

</dd> <dt>

*lpUserName* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a un búfer que contiene el nombre de usuario del nuevo usuario.

</dd> <dt>

*lpUserHive* \[ en, opcional\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a un búfer que contiene el [subárbol del Registro que se usará.](../sysinfo/registry-hives.md) Este parámetro puede ser **NULL**.

</dd> <dt>

*lpProfileDir* \[ out, opcional\]
</dt> <dd>

Tipo: **LPTSTR**

Puntero a un búfer que, cuando esta función vuelve, recibe la ruta de acceso del directorio del perfil del usuario. Este parámetro puede ser **NULL**.

</dd> <dt>

*dwDirSize* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Tamaño del búfer especificado por *lpProfileDir*, en TCHAR.

</dd> <dt>

*bWin9xUpg* \[ En\]
</dt> <dd>

Tipo: **BOOL**

**TRUE** si el perfil de usuario se crea como parte de una migración de perfil desde Windows 9x; de lo contrario, **FALSE**.

Cuando **es TRUE,** el perfil de usuario se configura en el directorio de perfil predeterminado, normalmente C: \\ Documents y Configuración \\ *UserName*. Si ese directorio ya existe, se usa. Si no es así, se crea.

Si **es FALSE,** se crea el directorio de perfil predeterminado si no existe. Si el directorio de perfil predeterminado ya existe, se crea un nuevo directorio para este perfil de usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Devuelve **TRUE** si el nuevo perfil de usuario se creó correctamente; de lo contrario, **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no se declara en los encabezados del Kit de desarrollo de software (SDK) y no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular a Userenv.dll. Se hace referencia a la versión ANSI de la función **CreateUserProfileExA** desde Userenv.dll como ordinal 153. Se hace referencia a la versión Unicode **CreateUserProfileExW** como ordinal 154.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/>  | Windows XP<br/>                                                                  |
| Archivo DLL<br/>                    | <dl> <dt>Userenv.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/> | **CreateUserProfileExW** (Unicode) y **CreateUserProfileExA** (ANSI)<br/>      |



 

 
