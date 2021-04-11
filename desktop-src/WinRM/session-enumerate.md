---
title: Método Session. Enumerate (WSManDisp. h)
description: Enumera una tabla, una colección de datos o un recurso de registro.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumerar Administración remota de Windows de método
- Enumerar Administración remota de Windows de método, objeto de sesión
- Objeto Session Administración remota de Windows, Enumerate (método)
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079143"
---
# <a name="sessionenumerate-method"></a><span data-ttu-id="0f3e1-106">Session. Enumerate (método)</span><span class="sxs-lookup"><span data-stu-id="0f3e1-106">Session.Enumerate method</span></span>

<span data-ttu-id="0f3e1-107">Enumera una tabla, una colección de datos o un recurso de registro.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-107">Enumerates a table, data collection, or log resource.</span></span> <span data-ttu-id="0f3e1-108">Para crear una consulta, incluya un parámetro de *filtro* y un parámetro de *dialecto* en una enumeración.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-108">To create a query, include a *filter* parameter and a *dialect* parameter in an enumeration.</span></span> <span data-ttu-id="0f3e1-109">También puede usar un objeto [**ResourceLocator**](resourcelocator.md) para crear consultas.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-109">You can also use a [**ResourceLocator**](resourcelocator.md) object to create queries.</span></span> <span data-ttu-id="0f3e1-110">Para obtener más información, consulte [enumeración o enumeración de todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="0f3e1-110">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3e1-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f3e1-111">Syntax</span></span>


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0f3e1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f3e1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3e1-113">*resourceUri* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f3e1-113">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3e1-114">Identificador del recurso que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-114">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="0f3e1-115">Este parámetro puede contener uno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="0f3e1-115">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="0f3e1-116">URI del recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-116">The URI of the resource.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   <span data-ttu-id="0f3e1-117">Objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="0f3e1-117">A [**ResourceLocator**](resourcelocator.md) object.</span></span>
-   <span data-ttu-id="0f3e1-118">Una referencia de extremo de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar del protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="0f3e1-119">Para obtener más información sobre la especificación pública de [protocolo WS-Management](ws-management-protocol.md), consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="0f3e1-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="0f3e1-120">*filtro* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f3e1-120">*filter* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3e1-121">Filtro que define los elementos del recurso devueltos por la enumeración.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-121">A filter that defines what items in the resource are returned by the enumeration.</span></span> <span data-ttu-id="0f3e1-122">Cuando se enumera el recurso, solo se devuelven los elementos que coinciden con los criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-122">When the resource is enumerated, only those items that match the filter criteria are returned.</span></span> <span data-ttu-id="0f3e1-123">Al incluir un parámetro de *filtro* y un parámetro de *dialecto* en una enumeración, la enumeración se convierte en una consulta.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-123">Including a *filter* parameter and a *dialect* parameter in an enumeration converts the enumeration into a query.</span></span> <span data-ttu-id="0f3e1-124">Para obtener un ejemplo, consulte [consultar instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="0f3e1-124">For an example, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

<span data-ttu-id="0f3e1-125">Si tiene un objeto [**ResourceLocator**](resourcelocator.md) para el parámetro *resourceURI* , este parámetro no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-125">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="0f3e1-126">*dialecto* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f3e1-126">*dialect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3e1-127">Lenguaje utilizado por el filtro.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-127">The language used by the filter.</span></span> <span data-ttu-id="0f3e1-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), un subconjunto de SQL utilizado por WMI, es el único lenguaje que se admite.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), a subset of SQL used by WMI, is the only language supported.</span></span>

<span data-ttu-id="0f3e1-129">Si tiene un objeto [**ResourceLocator**](resourcelocator.md) para el parámetro *resourceURI* , este parámetro no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-129">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="0f3e1-130">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f3e1-130">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3e1-131">Parámetro que debe contener una marca en la enumeración **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="0f3e1-131">A parameter that must contain a flag in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="0f3e1-132">Para obtener más información, vea [constantes de enumeración](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0f3e1-132">For more information, see [Enumeration Constants](enumeration-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f3e1-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f3e1-133">Return value</span></span>

<span data-ttu-id="0f3e1-134">Objeto de [**enumerador**](enumerator.md) que contiene los resultados de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-134">An [**Enumerator**](enumerator.md) object that contains the results of the enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f3e1-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f3e1-135">Remarks</span></span>

<span data-ttu-id="0f3e1-136">Para obtener más información sobre cómo limitar las llamadas de red durante una enumeración, vea la propiedad [**BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="0f3e1-136">For more information about limiting network calls during an enumeration, see the [**BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="0f3e1-137">Tenga en cuenta que si las marcas incluyen las [**constantes de enumeración**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , entonces administración remota de Windows servicio devuelve el error del código de error del **modo de \_ \_ polimorfismo WSMAN \_ \_ no compatible**.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-137">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then Windows Remote Management service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

<span data-ttu-id="0f3e1-138">Si se especifica un filtro, debe ser un documento válido con respecto al esquema del recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-138">If a filter is specified, it must be a valid document with respect to the schema of the resource.</span></span> <span data-ttu-id="0f3e1-139">El parámetro Dialect es opcional.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-139">The dialect parameter is optional.</span></span> <span data-ttu-id="0f3e1-140">Sin embargo, si la cadena de filtro comienza con <, pero no es un fragmento XML, incluya el parámetro de *dialecto* o establezca la marca **WSManFlagNonXmlText** en el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="0f3e1-140">However, if the filter string begins with <, but is not an XML fragment, then either include the *dialect* parameter or set the **WSManFlagNonXmlText** flag in the *flags* parameter.</span></span> <span data-ttu-id="0f3e1-141">Para obtener más información, vea [**constantes de enumeración**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0f3e1-141">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

<span data-ttu-id="0f3e1-142">El método de C++ correspondiente es [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="0f3e1-142">The corresponding C++ method is [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

## <a name="examples"></a><span data-ttu-id="0f3e1-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0f3e1-143">Examples</span></span>

<span data-ttu-id="0f3e1-144">En el siguiente ejemplo de código de VBScript se enumeran las instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en un equipo remoto especificado por el nombre de dominio completo (ServerName.domain.com).</span><span class="sxs-lookup"><span data-stu-id="0f3e1-144">The following VBScript code example enumerates the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instances on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="0f3e1-145">Tenga en cuenta que liberar el objeto de enumeración borra las solicitudes de enumeración pendientes.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-145">Be aware that freeing the enumeration object clears pending enumeration requests.</span></span> <span data-ttu-id="0f3e1-146">La subrutina DisplayOutput usa el archivo de transformación XML de la herramienta de línea de comandos de WinRM (WsmTxt. xsl) para generar los datos en un formato tabular.</span><span class="sxs-lookup"><span data-stu-id="0f3e1-146">The DisplayOutput subroutine uses the Winrm command-line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0f3e1-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f3e1-147">Requirements</span></span>



| <span data-ttu-id="0f3e1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f3e1-148">Requirement</span></span> | <span data-ttu-id="0f3e1-149">Value</span><span class="sxs-lookup"><span data-stu-id="0f3e1-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3e1-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f3e1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3e1-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f3e1-151">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0f3e1-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f3e1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3e1-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f3e1-153">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0f3e1-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f3e1-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3e1-155"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f3e1-155"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f3e1-156">IDL</span><span class="sxs-lookup"><span data-stu-id="0f3e1-156">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f3e1-157"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f3e1-157"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f3e1-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f3e1-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f3e1-159"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0f3e1-159"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0f3e1-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f3e1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3e1-161"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3e1-161"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f3e1-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f3e1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3e1-163">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="0f3e1-163">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="0f3e1-164">Consultar instancias específicas de un recurso</span><span class="sxs-lookup"><span data-stu-id="0f3e1-164">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="0f3e1-165">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="0f3e1-165">**BatchItems**</span></span>](session-batchitems.md)
</dt> <dt>

[<span data-ttu-id="0f3e1-166">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="0f3e1-166">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

