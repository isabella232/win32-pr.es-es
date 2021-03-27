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
# <a name="createuserprofileex-function"></a><span data-ttu-id="a7435-103">CreateUserProfileEx función)</span><span class="sxs-lookup"><span data-stu-id="a7435-103">CreateUserProfileEx function</span></span>

<span data-ttu-id="a7435-104">\[Esta función no está disponible en Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="a7435-104">\[This function is not available as of Windows Vista.\]</span></span>

<span data-ttu-id="a7435-105">Crea un perfil de usuario para un usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="a7435-105">Creates a user profile for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7435-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7435-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a7435-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7435-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7435-108">*pSid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7435-108">*pSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7435-109">Tipo: **psid**</span><span class="sxs-lookup"><span data-stu-id="a7435-109">Type: **PSID**</span></span>

<span data-ttu-id="a7435-110">SID del nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="a7435-110">The SID of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="a7435-111">*lpUserName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7435-111">*lpUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7435-112">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="a7435-112">Type: **LPCTSTR**</span></span>

<span data-ttu-id="a7435-113">Puntero a un búfer que contiene el nombre de usuario del nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="a7435-113">Pointer to a buffer that contains the user name of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="a7435-114">*lpUserHive* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a7435-114">*lpUserHive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7435-115">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="a7435-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="a7435-116">Puntero a un búfer que contiene el [subárbol del registro](../sysinfo/registry-hives.md) que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a7435-116">Pointer to a buffer that contains the [registry hive](../sysinfo/registry-hives.md) to use.</span></span> <span data-ttu-id="a7435-117">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a7435-117">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a7435-118">*lpProfileDir* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a7435-118">*lpProfileDir* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7435-119">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="a7435-119">Type: **LPTSTR**</span></span>

<span data-ttu-id="a7435-120">Puntero a un búfer que, cuando esta función devuelve, recibe la ruta de acceso del directorio del perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="a7435-120">Pointer to a buffer that, when this function returns, receives the user's profile directory path.</span></span> <span data-ttu-id="a7435-121">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a7435-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a7435-122">*dwDirSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7435-122">*dwDirSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7435-123">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a7435-123">Type: **DWORD**</span></span>

<span data-ttu-id="a7435-124">Tamaño del búfer especificado por *lpProfileDir*, en TCHARs.</span><span class="sxs-lookup"><span data-stu-id="a7435-124">Size of the buffer specified by *lpProfileDir*, in TCHARs.</span></span>

</dd> <dt>

<span data-ttu-id="a7435-125">*bWin9xUpg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7435-125">*bWin9xUpg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7435-126">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="a7435-126">Type: **BOOL**</span></span>

<span data-ttu-id="a7435-127">**True** si el perfil de usuario se crea como parte de una migración de perfil desde Windows 9x; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7435-127">**TRUE** if the user profile is being created as part of a profile migration from Windows 9x; otherwise, **FALSE**.</span></span>

<span data-ttu-id="a7435-128">Si es **true**, el perfil de usuario se configura en el directorio de perfil predeterminado, normalmente C: \\ Documents and Settings \\ *username*.</span><span class="sxs-lookup"><span data-stu-id="a7435-128">When **TRUE**, the user profile is set up in the default profile directory—normally C:\\Documents and Settings\\*UserName*.</span></span> <span data-ttu-id="a7435-129">Si ese directorio ya existe, se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a7435-129">If that directory already exists, it is used.</span></span> <span data-ttu-id="a7435-130">Si no es así, se crea.</span><span class="sxs-lookup"><span data-stu-id="a7435-130">If it does not, it is created.</span></span>

<span data-ttu-id="a7435-131">Si es **false**, se crea el directorio de perfil predeterminado si no existe.</span><span class="sxs-lookup"><span data-stu-id="a7435-131">If **FALSE**, the default profile directory is created if it does not exist.</span></span> <span data-ttu-id="a7435-132">Si el directorio de perfil predeterminado ya existe, se crea un nuevo directorio para este perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="a7435-132">If the default profile directory already exists, a new directory is created for this user profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7435-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7435-133">Return value</span></span>

<span data-ttu-id="a7435-134">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="a7435-134">Type: **BOOL**</span></span>

<span data-ttu-id="a7435-135">Devuelve **true** si el nuevo perfil de usuario se creó correctamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7435-135">Returns **TRUE** if the new user profile was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7435-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7435-136">Remarks</span></span>

<span data-ttu-id="a7435-137">Esta función no se declara en los encabezados del kit de desarrollo de software (SDK) y no tiene asociada ninguna biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="a7435-137">This function is not declared in the software development kit (SDK) headers and has no associated import library.</span></span> <span data-ttu-id="a7435-138">Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular a Userenv.dll.</span><span class="sxs-lookup"><span data-stu-id="a7435-138">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to link to Userenv.dll.</span></span> <span data-ttu-id="a7435-139">La versión ANSI de la función, a la que se hace referencia **CreateUserProfileExA** desde Userenv.dll como ordinal 153.</span><span class="sxs-lookup"><span data-stu-id="a7435-139">The ANSI version of the function, **CreateUserProfileExA** is referenced from Userenv.dll as ordinal 153.</span></span> <span data-ttu-id="a7435-140">En la versión Unicode, se hace referencia a **CreateUserProfileExW** como el ordinal 154.</span><span class="sxs-lookup"><span data-stu-id="a7435-140">The Unicode version, **CreateUserProfileExW** is referenced as ordinal 154.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7435-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7435-141">Requirements</span></span>



| <span data-ttu-id="a7435-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7435-142">Requirement</span></span> | <span data-ttu-id="a7435-143">Value</span><span class="sxs-lookup"><span data-stu-id="a7435-143">Value</span></span> |
|-----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7435-144">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a7435-144">End of client support</span></span><br/>  | <span data-ttu-id="a7435-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7435-145">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="a7435-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7435-146">DLL</span></span><br/>                    | <dl> <span data-ttu-id="a7435-147"><dt>Userenv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7435-147"><dt>Userenv.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7435-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a7435-148">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="a7435-149">**CreateUserProfileExW** (Unicode) y **CreateUserProfileExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a7435-149">**CreateUserProfileExW** (Unicode) and **CreateUserProfileExA** (ANSI)</span></span><br/>      |



 

 
