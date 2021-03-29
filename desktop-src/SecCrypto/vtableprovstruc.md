---
description: Contiene punteros a funciones de devolución de llamada que pueden usar las funciones del proveedor de servicios criptográficos (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Estructura VTableProvStruc (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817635"
---
# <a name="vtableprovstruc-structure"></a><span data-ttu-id="ab873-103">Estructura VTableProvStruc</span><span class="sxs-lookup"><span data-stu-id="ab873-103">VTableProvStruc structure</span></span>

<span data-ttu-id="ab873-104">La estructura **VTableProvStruc** contiene punteros a funciones de devolución de llamada que pueden usar las funciones del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="ab873-104">The **VTableProvStruc** structure contains pointers to callback functions that can be used by [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab873-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab873-105">Syntax</span></span>


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a><span data-ttu-id="ab873-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab873-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab873-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="ab873-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="ab873-108">Valor **DWORD** que indica la versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="ab873-108">A **DWORD** value that indicates the version of the structure.</span></span> <span data-ttu-id="ab873-109">Se usan tres versiones de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="ab873-109">Three versions of this structure are used.</span></span> <span data-ttu-id="ab873-110">Las versiones son los números 1, 2 y 3, y determinan qué miembros de la estructura son válidos.</span><span class="sxs-lookup"><span data-stu-id="ab873-110">The versions are number 1, 2, and 3, and determine which members of the structure are valid.</span></span> <span data-ttu-id="ab873-111">Los miembros de la versión 1 son válidos en todos los sistemas que admiten esta estructura.</span><span class="sxs-lookup"><span data-stu-id="ab873-111">Version 1 members are valid on all systems that support this structure.</span></span>

<span data-ttu-id="ab873-112">Se trata de un miembro de la versión 1.</span><span class="sxs-lookup"><span data-stu-id="ab873-112">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="ab873-113">**FuncVerifyImage**</span><span class="sxs-lookup"><span data-stu-id="ab873-113">**FuncVerifyImage**</span></span>
</dt> <dd>

<span data-ttu-id="ab873-114">La dirección de una función de devolución de llamada [**FuncVerifyImage**](funcverifyimage.md) que usa el CSP para comprobar la firma de los archivos DLL que el CSP va a cargar.</span><span class="sxs-lookup"><span data-stu-id="ab873-114">The address of a [**FuncVerifyImage**](funcverifyimage.md) callback function that the CSP uses to verify the signature of any DLLs that the CSP will load.</span></span> <span data-ttu-id="ab873-115">Todas las DLL auxiliares en las que un CSP realiza llamadas a funciones deben estar firmadas de la misma manera (y con la misma clave) que la DLL de CSP principal.</span><span class="sxs-lookup"><span data-stu-id="ab873-115">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="ab873-116">Para garantizar esta firma, los archivos dll auxiliares se deben cargar dinámicamente mediante la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="ab873-116">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="ab873-117">Pero antes de que se cargue el archivo DLL, se debe comprobar la firma de la DLL.</span><span class="sxs-lookup"><span data-stu-id="ab873-117">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="ab873-118">El CSP realiza esta comprobación mediante una llamada a la función **FuncVerifyImage** , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab873-118">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

<span data-ttu-id="ab873-119">Este puntero de función se puede almacenar y usar hasta que se libere el contexto CSP.</span><span class="sxs-lookup"><span data-stu-id="ab873-119">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="ab873-120">Se trata de un miembro de la versión 1.</span><span class="sxs-lookup"><span data-stu-id="ab873-120">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="ab873-121">**FuncReturnhWnd**</span><span class="sxs-lookup"><span data-stu-id="ab873-121">**FuncReturnhWnd**</span></span>
</dt> <dd>

<span data-ttu-id="ab873-122">La dirección de una función de devolución de llamada [**FuncReturnhWnd**](funcreturnhwnd.md) que devuelve el identificador de ventana que el CSP debe utilizar como elemento primario o propietario de cualquier interfaz de usuario que se muestre.</span><span class="sxs-lookup"><span data-stu-id="ab873-122">The address of a [**FuncReturnhWnd**](funcreturnhwnd.md) callback function that returns the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span> <span data-ttu-id="ab873-123">Los CSP que no se comunican directamente con el usuario y los CSP que usan Hardware dedicado para este propósito pueden omitir esta entrada.</span><span class="sxs-lookup"><span data-stu-id="ab873-123">CSPs that do not communicate directly with the user and CSPs that use dedicated hardware for this purpose can ignore this entry.</span></span> <span data-ttu-id="ab873-124">De forma predeterminada, este identificador de ventana es cero, pero una aplicación puede establecerlo en un valor diferente mediante la función [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) para establecer la propiedad **\_ \_ hWnd del cliente PP** .</span><span class="sxs-lookup"><span data-stu-id="ab873-124">This window handle is zero by default, but an application can set this to a different value by using the [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) function to set the **PP\_CLIENT\_HWND** property.</span></span>

<span data-ttu-id="ab873-125">Este puntero de función se puede almacenar y usar hasta que se libere el contexto CSP.</span><span class="sxs-lookup"><span data-stu-id="ab873-125">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="ab873-126">Se trata de un miembro de la versión 1.</span><span class="sxs-lookup"><span data-stu-id="ab873-126">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="ab873-127">**dwProvType**</span><span class="sxs-lookup"><span data-stu-id="ab873-127">**dwProvType**</span></span>
</dt> <dd>

<span data-ttu-id="ab873-128">Valor **DWORD** que especifica el tipo de proveedor que se va a adquirir.</span><span class="sxs-lookup"><span data-stu-id="ab873-128">A **DWORD** value that specifies the type of provider to acquire.</span></span> <span data-ttu-id="ab873-129">Los siguientes [*tipos de proveedor*](../secgloss/p-gly.md) están predefinidos y se describen en detalle en [interoperabilidad de CSP](https://www.bing.com/search?q=CSP+Interoperability):</span><span class="sxs-lookup"><span data-stu-id="ab873-129">The following [*provider types*](../secgloss/p-gly.md) are predefined and are discussed in detail in [CSP Interoperability](https://www.bing.com/search?q=CSP+Interoperability):</span></span>

-   <span data-ttu-id="ab873-130">aprovisionamiento \_ completo de RSA \_</span><span class="sxs-lookup"><span data-stu-id="ab873-130">PROV\_RSA\_FULL</span></span>
-   <span data-ttu-id="ab873-131">\_firma RSA \_ SIG</span><span class="sxs-lookup"><span data-stu-id="ab873-131">PROV\_RSA\_SIG</span></span>
-   <span data-ttu-id="ab873-132">DSS de PROV \_</span><span class="sxs-lookup"><span data-stu-id="ab873-132">PROV\_DSS</span></span>
-   <span data-ttu-id="ab873-133">Fortezza de PROV \_</span><span class="sxs-lookup"><span data-stu-id="ab873-133">PROV\_FORTEZZA</span></span>
-   <span data-ttu-id="ab873-134">\_Microsoft \_ Exchange</span><span class="sxs-lookup"><span data-stu-id="ab873-134">PROV\_MS\_EXCHANGE</span></span>

<span data-ttu-id="ab873-135">Este es un miembro de la versión 2.</span><span class="sxs-lookup"><span data-stu-id="ab873-135">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="ab873-136">**pbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="ab873-136">**pbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ab873-137">Puntero a una matriz de información de contexto.</span><span class="sxs-lookup"><span data-stu-id="ab873-137">A pointer to an array of context information.</span></span> <span data-ttu-id="ab873-138">Juntos, los miembros **pbContextInfo** y **cbContextInfo** determinan el conjunto de información que se usa cuando se llama a una función [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) con la información de contexto de PP \_ \_ establecida.</span><span class="sxs-lookup"><span data-stu-id="ab873-138">The **pbContextInfo** and **cbContextInfo** members together determine the information set used when a [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) function is called with PP\_CONTEXT\_INFO set.</span></span>

<span data-ttu-id="ab873-139">Este es un miembro de la versión 2.</span><span class="sxs-lookup"><span data-stu-id="ab873-139">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="ab873-140">**cbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="ab873-140">**cbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ab873-141">Valor **DWORD** que indica el número de elementos de la matriz **pbContextInfo** .</span><span class="sxs-lookup"><span data-stu-id="ab873-141">A **DWORD** value that indicates the number of elements in the **pbContextInfo** array.</span></span>

<span data-ttu-id="ab873-142">Este es un miembro de la versión 2.</span><span class="sxs-lookup"><span data-stu-id="ab873-142">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="ab873-143">**pszProvName**</span><span class="sxs-lookup"><span data-stu-id="ab873-143">**pszProvName**</span></span>
</dt> <dd>

<span data-ttu-id="ab873-144">Cadena que contiene el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ab873-144">A string that contains the name of the provider.</span></span>

<span data-ttu-id="ab873-145">Se trata de un miembro de la versión 3.</span><span class="sxs-lookup"><span data-stu-id="ab873-145">This is a version 3 member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab873-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab873-146">Remarks</span></span>

<span data-ttu-id="ab873-147">Los punteros de la estructura **VTableProvStruc** solo están disponibles dentro de la función [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) .</span><span class="sxs-lookup"><span data-stu-id="ab873-147">The pointers in the **VTableProvStruc** structure are only available within the [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) function.</span></span> <span data-ttu-id="ab873-148">Si los miembros de la estructura son necesarios después de que se complete una llamada a **CPAcquireContext** , el CSP debe realizar copias de los elementos de la estructura necesarios.</span><span class="sxs-lookup"><span data-stu-id="ab873-148">If members of the structure are needed after a call to **CPAcquireContext** is completed, copies of the needed structure elements must be made by the CSP.</span></span> <span data-ttu-id="ab873-149">Los punteros de función de esta estructura se pueden almacenar y usar hasta que se libere el contexto CSP.</span><span class="sxs-lookup"><span data-stu-id="ab873-149">The function pointers in this structure can be stored and used until the CSP context is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab873-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab873-150">Requirements</span></span>



| <span data-ttu-id="ab873-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab873-151">Requirement</span></span> | <span data-ttu-id="ab873-152">Value</span><span class="sxs-lookup"><span data-stu-id="ab873-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab873-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab873-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ab873-154">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ab873-154">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab873-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab873-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ab873-156">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab873-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ab873-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab873-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab873-158"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab873-158"><dt>Cspdk.h</dt></span></span> </dl> |
| <span data-ttu-id="ab873-159">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ab873-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ab873-160">**VTableProvStrucW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="ab873-160">**VTableProvStrucW** (Unicode)</span></span><br/>                                          |



 

 
