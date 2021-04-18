---
description: Recupera el nombre de clase y otra información asociada a un GUID determinado en el manifiesto de un componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649637"
---
# <a name="sxslookupclrguid-function"></a><span data-ttu-id="073f7-103">SxsLookupClrGuid función)</span><span class="sxs-lookup"><span data-stu-id="073f7-103">SxsLookupClrGuid function</span></span>

<span data-ttu-id="073f7-104">Recupera el nombre de clase y otra información asociada a un GUID determinado en el manifiesto de un componente.</span><span class="sxs-lookup"><span data-stu-id="073f7-104">Retrieves the class name and other information associated with a given GUID in a component's manifest.</span></span> <span data-ttu-id="073f7-105">Esta función solo se usa al implementar la interoperabilidad administrada no administrada de bajo nivel en el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="073f7-105">This function is used only when implementing low-level managed-unmanaged interoperability in the .NET Framework.</span></span> <span data-ttu-id="073f7-106">Para obtener más información sobre la interoperabilidad administrada y no administrada, vea "interoperar con código no administrado" en el SDK de .NET Framework y también en [aplicaciones aisladas y ensamblados en paralelo](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="073f7-106">For more information about managed-unmanaged interoperability, see "Interoperating with Unmanaged Code" in the .NET Framework SDK and also [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="073f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="073f7-107">Syntax</span></span>


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="073f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="073f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="073f7-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="073f7-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073f7-110">Combinación de cero o más de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="073f7-110">A combination of zero or more of the following flags.</span></span>



| <span data-ttu-id="073f7-111">Value</span><span class="sxs-lookup"><span data-stu-id="073f7-111">Value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="073f7-112">Significado</span><span class="sxs-lookup"><span data-stu-id="073f7-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <span data-ttu-id="073f7-113"><dt>**SxS \_ BUSCAR \_ GUID de CLR \_ \_ use \_ ACTCTX**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="073f7-113"><dt>**SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX**</dt> <dt>0x00000001</dt></span></span> </dl>              | <span data-ttu-id="073f7-114">Si se establece esta marca, el parámetro *hActCtx* debe contener un identificador de contexto de activación devuelto por la función [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="073f7-114">If this flag is set, then the *hActCtx* parameter must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="073f7-115">Si no se establece esta marca, se omite el parámetro *hActCtx* y **SxsLookupClrGuid** busca en el contexto de activación que está activo actualmente (la función [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) se usa para activar un contexto de activación).</span><span class="sxs-lookup"><span data-stu-id="073f7-115">If this flag is not set, the *hActCtx* parameter is ignored and **SxsLookupClrGuid** searches the activation context that is currently active (the [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) function is used to make an activation context active).</span></span><br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <span data-ttu-id="073f7-116"><dt>**SxS \_ \_ \_ Buscar GUID de CLR \_ busque \_ suplente**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="073f7-116"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE**</dt> <dt>0x00010000</dt></span></span> </dl>  | <span data-ttu-id="073f7-117">Si se establece esta marca, **SxsLookupClrGuid** busca un suplente.</span><span class="sxs-lookup"><span data-stu-id="073f7-117">If this flag is set, **SxsLookupClrGuid** searches for a surrogate.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <span data-ttu-id="073f7-118"><dt>**SxS \_ \_Buscar GUID de CLR búsqueda de \_ \_ \_ \_ clase CLR**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="073f7-118"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="073f7-119">Si se establece esta marca, **SxsLookupClrGuid** busca una clase.</span><span class="sxs-lookup"><span data-stu-id="073f7-119">If this flag is set, **SxsLookupClrGuid** searches for a class.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <span data-ttu-id="073f7-120"><dt>**SxS \_ \_ \_ Buscar GUID de CLR \_ busque \_ cualquier**</dt> <dt>0x00030000</dt></span><span class="sxs-lookup"><span data-stu-id="073f7-120"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_ANY**</dt> <dt>0x00030000</dt></span></span> </dl>                    | <span data-ttu-id="073f7-121">Se trata de una combinación del GUID de CLR de búsqueda en paralelo. buscar el GUID de CLR de búsqueda **\_ \_ \_ \_ \_ suplente** y SxS buscar las marcas  de **\_ \_ \_ \_ \_ \_ clase de CLR** ; si ambos están establecidos, SxsLookupClrGuid busca un suplente primero y, solo si no encuentra uno, busca una clase.</span><span class="sxs-lookup"><span data-stu-id="073f7-121">This is a combination of the **SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE** and **SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS** flags; if both are set, **SxsLookupClrGuid** searches for a surrogate first, and only if it does not find one, then searches for a class.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="073f7-122">*pClsid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="073f7-122">*pClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073f7-123">Puntero al GUID en el que se va a buscar información de interoperación en el contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="073f7-123">A pointer to the GUID about which to search the activation context for interoperation information.</span></span> <span data-ttu-id="073f7-124">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="073f7-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="073f7-125">*hActCtx* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="073f7-125">*hActCtx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="073f7-126">Si el **\_ GUID de CLR de búsqueda SxS \_ \_ \_ usa \_** la marca ACTCTX se establece en el parámetro *dwFlags* , *hActCtx* debe contener un identificador de contexto de activación devuelto por la función [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="073f7-126">If the **SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX** flag is set in the *dwFlags* parameter, then *hActCtx* must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="073f7-127">De lo contrario, *hActCtx* se omite.</span><span class="sxs-lookup"><span data-stu-id="073f7-127">Otherwise, *hActCtx* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="073f7-128">*pvOutputBuffer* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="073f7-128">*pvOutputBuffer* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="073f7-129">Puntero al búfer en el que se copia la información de devolución.</span><span class="sxs-lookup"><span data-stu-id="073f7-129">Pointer to the buffer into which return information is copied.</span></span> <span data-ttu-id="073f7-130">Este parámetro solo puede tener valores NULL si el parámetro *cbOutputBuffer* tiene un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="073f7-130">This parameter may be NULL-valued only if the *cbOutputBuffer* parameter is zero-valued.</span></span> <span data-ttu-id="073f7-131">Los datos colocados en este búfer al salir (si los hay) se componen de una estructura **\_ CLR de \_ información \_ de GUID SxS** seguida de cualquier dato de cadena adicional requerido.</span><span class="sxs-lookup"><span data-stu-id="073f7-131">The data placed in this buffer on exit (if any) consists of a **SXS\_GUID\_INFORMATION\_CLR** structure followed by any additional string data required.</span></span> <span data-ttu-id="073f7-132">Vea la sección comentarios que aparece a continuación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="073f7-132">See the Remarks section below for more information.</span></span>

</dd> <dt>

<span data-ttu-id="073f7-133">*cbOutputBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="073f7-133">*cbOutputBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="073f7-134">Tamaño en bytes del búfer al que apunta el parámetro *pvOutputBuffer* .</span><span class="sxs-lookup"><span data-stu-id="073f7-134">Size in bytes of the buffer pointed to by the *pvOutputBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="073f7-135">*pcbOutputBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="073f7-135">*pcbOutputBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="073f7-136">Puntero a una variable en la que el tamaño, en bytes, de la información de devolución se coloca al salir.</span><span class="sxs-lookup"><span data-stu-id="073f7-136">Pointer to a variable where the size, in bytes, of the return information is placed on exit.</span></span> <span data-ttu-id="073f7-137">Si el parámetro *cbOutputBuffer* es cero, o si el tamaño del búfer de salida es menor que el tamaño de la información devuelta, se produce un error en **SxsLookupClrGuid** y [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de **\_ \_ búfer insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="073f7-137">If the *cbOutputBuffer* parameter is zero, or if the size of the output buffer is smaller than the size of the return information, then **SxsLookupClrGuid** fails and [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns an error of **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="073f7-138">En este caso, use el valor de la variable a la que apunta *pcbOutputBuffer* para asignar un búfer suficientemente grande y, a continuación, llame de nuevo a **SxsLookupClrGuid** para recuperar la información deseada.</span><span class="sxs-lookup"><span data-stu-id="073f7-138">In this case, use the value in the variable pointed to by *pcbOutputBuffer* to allocate a large enough buffer, and then call **SxsLookupClrGuid** again to retrieve the desired information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="073f7-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="073f7-139">Return value</span></span>

<span data-ttu-id="073f7-140">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="073f7-140">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="073f7-141">Para obtener más información sobre el error, llame a [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="073f7-141">For more error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>

## <a name="remarks"></a><span data-ttu-id="073f7-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="073f7-142">Remarks</span></span>

<span data-ttu-id="073f7-143">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="073f7-143">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="073f7-144">Los componentes administrados se pueden declarar como compatibles con "ensamblados de interoperabilidad" administrados para permitir que un consumidor de componentes Win32 no administrados haga referencia al ensamblado declarativo.</span><span class="sxs-lookup"><span data-stu-id="073f7-144">Managed components may declare themselves as supporting managed "interop assemblies" so as to allow an unmanaged Win32 component consumer to reference the declaring assembly.</span></span> <span data-ttu-id="073f7-145">El consumidor de componentes puede interactuar con el componente administrado llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en un GUID.</span><span class="sxs-lookup"><span data-stu-id="073f7-145">The component consumer can interact with the managed component by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on a GUID.</span></span> <span data-ttu-id="073f7-146">La capa de interoperación enruta la solicitud de creación de objeto a .NET Framework, crea una instancia del objeto administrado y devuelve un puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="073f7-146">The interoperation layer routes the object creation request to .NET Framework, creates an instance of the managed object, and returns an interface pointer.</span></span>

<span data-ttu-id="073f7-147">**SxsLookupClrGuid** permite que los marcos de trabajo recuperen información asociada a un GUID determinado en el manifiesto del componente, como cuál es su nombre de clase .net, qué versión del .NET Framework requiere y en qué ensamblado se encuentra.</span><span class="sxs-lookup"><span data-stu-id="073f7-147">**SxsLookupClrGuid** allows the frameworks to retrieve information associated with a given GUID in the component's manifest, such as what its .NET class name is, what version of the .NET Framework it requires, and what host assembly it is located in.</span></span> <span data-ttu-id="073f7-148">Los componentes administrados publican un ensamblado de interoperabilidad que contiene una serie de instrucciones que asocian los GUID con los nombres de ensamblado y tipo, y el tiempo de ejecución de .NET intercambia la construcción de instancias de objeto administradas cuando se llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="073f7-148">Managed components publish an interop assembly that contains a number of statements associating GUIDs with assembly and type names, and the .NET runtime brokers the construction of managed object instances when [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is called.</span></span>

<span data-ttu-id="073f7-149">A continuación se muestra un manifiesto de componente de ejemplo que declara un GUID de CLR y un suplente de CLR que **SxsLookupClrGuid** puede buscar:</span><span class="sxs-lookup"><span data-stu-id="073f7-149">The following is a sample component manifest declaring a CLR GUID and a CLR surrogate that **SxsLookupClrGuid** can look up:</span></span>

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

<span data-ttu-id="073f7-150">Un proveedor de interoperación llamaría a **SxsLookupClrGuid** con un puntero al GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" y recibiría en devolución el nombre de clase "MySampleSurrogate", la versión de tiempo de ejecución "1.0.3055" necesaria y la identidad de texto "dotnet. sample. suplentes, version = ' 1.0.0.0 ', Type = ' Interop '" del componente de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="073f7-150">An interoperation provider would call **SxsLookupClrGuid** with a pointer to the GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", and would receive in return the class name "MySampleSurrogate", the required runtime version "1.0.3055", and the textual identity "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" of the hosting component.</span></span>

<span data-ttu-id="073f7-151">Esta información de devolución se incluiría o se hacer referencia a ella mediante una estructura **\_ CLR de \_ información \_ de GUID SxS** declarada como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="073f7-151">This return information would be contained and/or referenced by a **SXS\_GUID\_INFORMATION\_CLR** structure declared as follows.</span></span>

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

<span data-ttu-id="073f7-152">Los miembros de esta estructura contienen la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="073f7-152">The members of this structure contain the following information.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="073f7-153">Miembro</span><span class="sxs-lookup"><span data-stu-id="073f7-153">Member</span></span></th>
<th><span data-ttu-id="073f7-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="073f7-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="073f7-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span><span class="sxs-lookup"><span data-stu-id="073f7-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span></span><br/></td>
<td><span data-ttu-id="073f7-156">Contiene el tamaño de la estructura de SXS_GUID_INFORMATION_CLR (esto permite que la estructura crezca en versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="073f7-156">Contains the size of the SXS_GUID_INFORMATION_CLR structure (this allows the structure to grow in later versions).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073f7-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span><span class="sxs-lookup"><span data-stu-id="073f7-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span></span><br/></td>
<td><span data-ttu-id="073f7-158">Contiene uno de los dos valores de marca siguientes:</span><span class="sxs-lookup"><span data-stu-id="073f7-158">Contains one of the following two flag values:</span></span> <br/>
<ul>
<li><span data-ttu-id="073f7-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica que el GUID especificado estaba asociado a un &quot; suplente.&quot;</span><span class="sxs-lookup"><span data-stu-id="073f7-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Indicates that the specified GUID was associated with a &quot;surrogate.&quot;</span></span></li>
<li><span data-ttu-id="073f7-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica que el GUID especificado estaba asociado a una &quot; clase.&quot;</span><span class="sxs-lookup"><span data-stu-id="073f7-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Indicates that the specified GUID was associated with a &quot;class.&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073f7-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span><span class="sxs-lookup"><span data-stu-id="073f7-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span></span><br/></td>
<td><span data-ttu-id="073f7-162">Apunta a una cadena de caracteres anchos terminada en cero que identifica la versión del tiempo de ejecución especificado en el manifiesto del host para esta clase.</span><span class="sxs-lookup"><span data-stu-id="073f7-162">Points to a zero-terminated wide-character string that identifies the version of the runtime specified in the host manifest for this class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073f7-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="073f7-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span></span><br/></td>
<td><span data-ttu-id="073f7-164">Apunta a una cadena de caracteres anchos terminada en cero que contiene el nombre de la clase .NET asociada al GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="073f7-164">Points to a zero-terminated wide-character string that contains the name of the .NET class associated with the specified GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073f7-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="073f7-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span></span><br/></td>
<td><span data-ttu-id="073f7-166">Apunta a una cadena de caracteres anchos terminada en cero que contiene la identidad textual del ensamblado que hospeda esta clase.</span><span class="sxs-lookup"><span data-stu-id="073f7-166">Points to a zero-terminated wide-character string that contains the textual identity of the assembly that hosts this class.</span></span> <span data-ttu-id="073f7-167">Para obtener más información sobre la identidad textual, vea &quot; especificar nombres de tipo completos &quot; en &quot; detectar información de tipo en tiempo de ejecución en &quot; &quot; programación con el .NET Framework &quot; en el SDK de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="073f7-167">For more information about textual identity, see &quot;Specifying Fully Qualified Type Names&quot; under &quot;Discovering Type Information at Run Time&quot; under &quot;Programming with the .NET Framework&quot; in the .NET Framework SDK.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="073f7-168">Una aplicación no administrada puede usar la información devuelta de este modo para cargar la versión correcta del .NET Framework, cargar el ensamblado identificado por el elemento **pcwszAssemblyIdentity** y, a continuación, crear una instancia de la clase denominada por el elemento **pcwszTypeName** .</span><span class="sxs-lookup"><span data-stu-id="073f7-168">An unmanaged application can use the information returned in this fashion to load the right version of the .NET Framework, load the assembly identified by the **pcwszAssemblyIdentity** element, and then create an instance of the class named by the **pcwszTypeName** element.</span></span>

## <a name="examples"></a><span data-ttu-id="073f7-169">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="073f7-169">Examples</span></span>

<span data-ttu-id="073f7-170">Utilice la vinculación dinámica como se indica a continuación para llamar a la función **SxsLookupClrGuid** :</span><span class="sxs-lookup"><span data-stu-id="073f7-170">Use dynamic linking as follows to call the **SxsLookupClrGuid** function:</span></span>


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a><span data-ttu-id="073f7-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="073f7-171">Requirements</span></span>



| <span data-ttu-id="073f7-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="073f7-172">Requirement</span></span> | <span data-ttu-id="073f7-173">Value</span><span class="sxs-lookup"><span data-stu-id="073f7-173">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="073f7-174">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="073f7-174">DLL</span></span><br/> | <dl> <span data-ttu-id="073f7-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="073f7-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="073f7-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="073f7-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073f7-177">Aplicaciones aisladas y ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="073f7-177">Isolated Applications and Side-by-side Assemblies</span></span>](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[<span data-ttu-id="073f7-178">**CreateActCtx**</span><span class="sxs-lookup"><span data-stu-id="073f7-178">**CreateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[<span data-ttu-id="073f7-179">**ActivateActCtx**</span><span class="sxs-lookup"><span data-stu-id="073f7-179">**ActivateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[<span data-ttu-id="073f7-180">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="073f7-180">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
