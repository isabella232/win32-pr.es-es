---
UID: ''
title: SHGetFolderPathEx función)
description: Recupera la ruta de acceso de una carpeta conocida identificada por KNOWNFOLDERID.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104983947"
---
# <a name="shgetfolderpathex-function"></a><span data-ttu-id="a8380-103">SHGetFolderPathEx función)</span><span class="sxs-lookup"><span data-stu-id="a8380-103">SHGetFolderPathEx function</span></span>

## <a name="description"></a><span data-ttu-id="a8380-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8380-104">Description</span></span>

<span data-ttu-id="a8380-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a8380-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>
<span data-ttu-id="a8380-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a8380-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a8380-107">Recupera la ruta de acceso completa de una carpeta conocida identificada por el [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a8380-107">Retrieves the full path of a known folder identified by the folder's [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).</span></span>
<span data-ttu-id="a8380-108">Esto extiende [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) permitiendo establecer el tamaño inicial del búfer de cadena.</span><span class="sxs-lookup"><span data-stu-id="a8380-108">This extends [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) by allowing you to set the initial size of the string buffer.</span></span>

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a><span data-ttu-id="a8380-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8380-109">Parameters</span></span>

### <a name="rfid-in"></a><span data-ttu-id="a8380-110">RFID [in]</span><span class="sxs-lookup"><span data-stu-id="a8380-110">rfid [in]</span></span>

<span data-ttu-id="a8380-111">Referencia a **KNOWNFOLDERID** que identifica la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a8380-111">A reference to the **KNOWNFOLDERID** that identifies the folder.</span></span>

### <a name="dwflags-in"></a><span data-ttu-id="a8380-112">dwFlags [in]</span><span class="sxs-lookup"><span data-stu-id="a8380-112">dwFlags [in]</span></span>

<span data-ttu-id="a8380-113">Marcas que especifican opciones de recuperación especiales.</span><span class="sxs-lookup"><span data-stu-id="a8380-113">Flags that specify special retrieval options.</span></span>
<span data-ttu-id="a8380-114">Este valor puede ser 0; de lo contrario, uno o varios de los valores de [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .</span><span class="sxs-lookup"><span data-stu-id="a8380-114">This value can be 0; otherwise, one or more of the [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) values.</span></span>

### <a name="htoken-in-optional"></a><span data-ttu-id="a8380-115">hToken [in, Optional]</span><span class="sxs-lookup"><span data-stu-id="a8380-115">hToken [in, optional]</span></span>

<span data-ttu-id="a8380-116">Un [token de acceso](/windows/desktop/SecAuthZ/access-tokens) que representa a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="a8380-116">An [access token](/windows/desktop/SecAuthZ/access-tokens) that represents a particular user.</span></span>
<span data-ttu-id="a8380-117">Si este parámetro es **null**, que es el uso más común, la función solicita la carpeta conocida para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="a8380-117">If this parameter is **NULL**, which is the most common usage, the function requests the known folder for the current user.</span></span>

<span data-ttu-id="a8380-118">Solicite una carpeta de usuario específica pasando el *hToken* de ese usuario.</span><span class="sxs-lookup"><span data-stu-id="a8380-118">Request a specific user's folder by passing the *hToken* of that user.</span></span>
<span data-ttu-id="a8380-119">Esto se hace normalmente en el contexto de un servicio que tiene privilegios suficientes para recuperar el token de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="a8380-119">This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user.</span></span>
<span data-ttu-id="a8380-120">Dicho token debe abrirse con derechos [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) y [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .</span><span class="sxs-lookup"><span data-stu-id="a8380-120">That token must be opened with [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) and [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) rights.</span></span>
<span data-ttu-id="a8380-121">En algunos casos, también debe incluir [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span><span class="sxs-lookup"><span data-stu-id="a8380-121">In some cases, you also need to include [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span></span>
<span data-ttu-id="a8380-122">Además de pasar el *hToken* del usuario, se debe montar el subárbol del registro de ese usuario específico.</span><span class="sxs-lookup"><span data-stu-id="a8380-122">In addition to passing the user's *hToken*, the registry hive of that specific user must be mounted.</span></span>
<span data-ttu-id="a8380-123">Consulte [Access Control](/windows/desktop/SecAuthZ/access-control) para obtener más información sobre los problemas de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="a8380-123">See [Access Control](/windows/desktop/SecAuthZ/access-control) for further discussion of access control issues.</span></span>

<span data-ttu-id="a8380-124">Al asignar el parámetro *hToken* un valor de-1, se indica el usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a8380-124">Assigning the *hToken* parameter a value of -1 indicates the Default User.</span></span>
<span data-ttu-id="a8380-125">Esto permite a los clientes de [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) buscar ubicaciones de carpetas (por ejemplo, la carpeta **escritorio** ) del usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a8380-125">This allows clients of [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) to find folder locations (such as the **Desktop** folder) for the Default User.</span></span>
<span data-ttu-id="a8380-126">El perfil de usuario de usuario predeterminado se duplica cuando se crea una cuenta de usuario nueva e incluye carpetas especiales como **documentos** y **escritorio**.</span><span class="sxs-lookup"><span data-stu-id="a8380-126">The Default User user profile is duplicated when any new user account is created, and includes special folders such as **Documents** and **Desktop**.</span></span>
<span data-ttu-id="a8380-127">Los elementos agregados a la carpeta de usuario predeterminada también aparecen en cualquier cuenta de usuario nueva.</span><span class="sxs-lookup"><span data-stu-id="a8380-127">Any items added to the Default User folder also appear in any new user account.</span></span>
<span data-ttu-id="a8380-128">Tenga en cuenta que el acceso a las carpetas de usuario predeterminadas requiere privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="a8380-128">Note that access to the Default User folders requires administrator privileges.</span></span>

### <a name="pszpath-out"></a><span data-ttu-id="a8380-129">pszPath [out]</span><span class="sxs-lookup"><span data-stu-id="a8380-129">pszPath [out]</span></span>

<span data-ttu-id="a8380-130">Una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="a8380-130">A null-terminated, Unicode string.</span></span>
<span data-ttu-id="a8380-131">Este búfer debe tener el tamaño cchPath.</span><span class="sxs-lookup"><span data-stu-id="a8380-131">This buffer must be of size cchPath.</span></span>
<span data-ttu-id="a8380-132">Cuando **SHGetFolderPathEx** se devuelve correctamente, este parámetro contiene la ruta de acceso de la carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="a8380-132">When **SHGetFolderPathEx** returns successfully, this parameter contains the path for the known folder.</span></span>

### <a name="cchpath-in"></a><span data-ttu-id="a8380-133">cchPath [in]</span><span class="sxs-lookup"><span data-stu-id="a8380-133">cchPath [in]</span></span>

<span data-ttu-id="a8380-134">Tamaño del búfer de *ppszPath* , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="a8380-134">The size of the *ppszPath* buffer, in characters.</span></span>

## <a name="returns"></a><span data-ttu-id="a8380-135">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="a8380-135">Returns</span></span>

<span data-ttu-id="a8380-136">Devuelve **S_OK** si se realiza correctamente, o un valor de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a8380-136">Returns **S_OK** if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8380-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8380-137">Remarks</span></span>

<span data-ttu-id="a8380-138">Como [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) es un contenedor para [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), esta función (**SHGetFolderPathEx**) también sirve como extensión a **SHGetFolderPath**.</span><span class="sxs-lookup"><span data-stu-id="a8380-138">Since [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) is a wrapper for [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), this function (**SHGetFolderPathEx**) also serves as an extension to **SHGetFolderPath**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8380-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8380-139">See also</span></span>

[<span data-ttu-id="a8380-140">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="a8380-140">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)

[<span data-ttu-id="a8380-141">KNOWN_FOLDER_FLAG</span><span class="sxs-lookup"><span data-stu-id="a8380-141">KNOWN_FOLDER_FLAG</span></span>](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[<span data-ttu-id="a8380-142">SHGetFolderPath</span><span class="sxs-lookup"><span data-stu-id="a8380-142">SHGetFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[<span data-ttu-id="a8380-143">SHGetKnownFolderIDList</span><span class="sxs-lookup"><span data-stu-id="a8380-143">SHGetKnownFolderIDList</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[<span data-ttu-id="a8380-144">SHGetKnownFolderPath</span><span class="sxs-lookup"><span data-stu-id="a8380-144">SHGetKnownFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
