---
title: Método Session. Create (WSManDisp. h)
description: Crea una nueva instancia de un recurso y devuelve la referencia de extremo (EPR) del nuevo objeto.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Crear método Administración remota de Windows
- Create Method Administración remota de Windows, Session (objeto)
- Administración remota de Windows de objeto de sesión, Create (método)
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491578"
---
# <a name="sessioncreate-method"></a><span data-ttu-id="527d9-106">Método Session. Create</span><span class="sxs-lookup"><span data-stu-id="527d9-106">Session.Create method</span></span>

<span data-ttu-id="527d9-107">Crea una nueva instancia de un recurso y devuelve la [*referencia de extremo (EPR)*](windows-remote-management-glossary.md) del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="527d9-107">Creates a new instance of a resource and returns the [*endpoint reference (EPR)*](windows-remote-management-glossary.md) of the new object.</span></span>

## <a name="syntax"></a><span data-ttu-id="527d9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="527d9-108">Syntax</span></span>


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="527d9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="527d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527d9-110">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="527d9-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527d9-111">Identificador del recurso que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="527d9-111">Identifier of the resource to create.</span></span>

<span data-ttu-id="527d9-112">Este parámetro puede contener uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="527d9-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="527d9-113">URI con uno o más [*selectores*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="527d9-113">URI with one or more [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="527d9-114">Tenga en cuenta que el [*complemento WMI*](windows-remote-management-glossary.md) no admite la creación de ningún recurso que no sea un agente de escucha de [protocolo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="527d9-114">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a [WS-Management Protocol](ws-management-protocol.md) listener.</span></span>
-   <span data-ttu-id="527d9-115">Objeto [**ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*Opciones*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="527d9-115">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="527d9-116">Referencia de extremo de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar del protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="527d9-116">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="527d9-117">Para obtener más información acerca de la especificación pública para el protocolo de WS-Management, consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="527d9-117">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="527d9-118">*resource*</span><span class="sxs-lookup"><span data-stu-id="527d9-118">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="527d9-119">El XML que contiene el contenido del recurso.</span><span class="sxs-lookup"><span data-stu-id="527d9-119">The XML that contains resource content.</span></span>

</dd> <dt>

<span data-ttu-id="527d9-120">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="527d9-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="527d9-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="527d9-121">Reserved.</span></span> <span data-ttu-id="527d9-122">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="527d9-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="527d9-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="527d9-123">Return value</span></span>

<span data-ttu-id="527d9-124">El EPR del nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="527d9-124">The EPR of the new resource.</span></span>

## <a name="remarks"></a><span data-ttu-id="527d9-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="527d9-125">Remarks</span></span>

<span data-ttu-id="527d9-126">**Session. Create** solo se usa para crear nuevas instancias de un recurso.</span><span class="sxs-lookup"><span data-stu-id="527d9-126">**Session.Create** is only used for creating new instances of a resource.</span></span> <span data-ttu-id="527d9-127">Use el método [**Session. put**](session-put.md) para actualizar las instancias existentes de un recurso.</span><span class="sxs-lookup"><span data-stu-id="527d9-127">Use the [**Session.Put**](session-put.md) method to update existing instances of a resource.</span></span> <span data-ttu-id="527d9-128">Después de obtener el nuevo URI de recurso, puede llamar a [**Session. Get**](session-get.md) para recuperar el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="527d9-128">After you obtain the new resource URI, you can call [**Session.Get**](session-get.md) to retrieve the new object.</span></span> <span data-ttu-id="527d9-129">El nuevo objeto contiene las propiedades que el proveedor de recursos asigna al crear el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="527d9-129">The new object contains any properties that the resource provider assigns when creating the new object.</span></span> <span data-ttu-id="527d9-130">Por ejemplo, si crea una nueva [*escucha*](windows-remote-management-glossary.md) de protocolo de WS-Management y recupera el objeto de agente de escucha mediante **Session. Get**, también obtendrá las **propiedades Port**, **Enabled** y **ListenOn** .</span><span class="sxs-lookup"><span data-stu-id="527d9-130">For example, if you create a new WS-Management protocol [*listener*](windows-remote-management-glossary.md) and retrieve the listener object using **Session.Get**, then you also obtain the **Port**, **Enabled**, and **ListeningOn** properties.</span></span>

<span data-ttu-id="527d9-131">Tenga en cuenta que el [*complemento WMI*](windows-remote-management-glossary.md) no admite la creación de ningún recurso que no sea un agente de escucha del protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="527d9-131">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a WS-Management protocol listener.</span></span>

<span data-ttu-id="527d9-132">La siguiente sintaxis se usa para llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="527d9-132">The following syntax is used to call this method.</span></span>


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a><span data-ttu-id="527d9-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="527d9-133">Examples</span></span>

<span data-ttu-id="527d9-134">El siguiente ejemplo de código de VBScript llama a **Session. Create** para crear un agente de escucha en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="527d9-134">The following VBScript code example calls **Session.Create** to create a listener on the local computer.</span></span>


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a><span data-ttu-id="527d9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="527d9-135">Requirements</span></span>



| <span data-ttu-id="527d9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="527d9-136">Requirement</span></span> | <span data-ttu-id="527d9-137">Value</span><span class="sxs-lookup"><span data-stu-id="527d9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="527d9-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="527d9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="527d9-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="527d9-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="527d9-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="527d9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="527d9-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="527d9-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="527d9-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="527d9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="527d9-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="527d9-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="527d9-144">IDL</span><span class="sxs-lookup"><span data-stu-id="527d9-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="527d9-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="527d9-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="527d9-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="527d9-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="527d9-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="527d9-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="527d9-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="527d9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="527d9-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="527d9-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="527d9-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="527d9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527d9-151">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="527d9-151">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="527d9-152">Protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="527d9-152">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

