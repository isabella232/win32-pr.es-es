---
title: Enumerador. ReadItem (método) (WSManDisp. h)
description: Recupera un elemento del recurso y devuelve una representación XML del elemento.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Método ReadItem Administración remota de Windows
- Método ReadItem Administración remota de Windows, objeto Enumerator
- Objeto enumerador Administración remota de Windows, método ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079144"
---
# <a name="enumeratorreaditem-method"></a><span data-ttu-id="fed84-106">Enumerador. ReadItem (método)</span><span class="sxs-lookup"><span data-stu-id="fed84-106">Enumerator.ReadItem method</span></span>

<span data-ttu-id="fed84-107">Recupera un elemento del recurso y devuelve una representación XML del elemento.</span><span class="sxs-lookup"><span data-stu-id="fed84-107">Retrieves an item from the resource and returns an XML representation of the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed84-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fed84-108">Syntax</span></span>


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a><span data-ttu-id="fed84-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fed84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed84-110">*resource*</span><span class="sxs-lookup"><span data-stu-id="fed84-110">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="fed84-111">URI del elemento.</span><span class="sxs-lookup"><span data-stu-id="fed84-111">The URI of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed84-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fed84-112">Return value</span></span>

<span data-ttu-id="fed84-113">Representación XML del elemento.</span><span class="sxs-lookup"><span data-stu-id="fed84-113">The XML representation of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="fed84-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fed84-114">Remarks</span></span>

<span data-ttu-id="fed84-115">Para limitar el número de elementos que se leen, establezca la propiedad [**Session.BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="fed84-115">To limit the number of items that are read, set the [**Session.BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="fed84-116">Tenga en cuenta que la liberación del objeto de enumeración limpia todas las solicitudes de enumeración pendientes.</span><span class="sxs-lookup"><span data-stu-id="fed84-116">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span>

<span data-ttu-id="fed84-117">El método [**Session. Enumerate**](session-enumerate.md) no obtiene una colección de la misma manera que una [consulta WMI](/windows/desktop/WmiSdk/querying-wmi), como `SELECT * from Win32_LogicalDisk` , devuelve una colección en un [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span><span class="sxs-lookup"><span data-stu-id="fed84-117">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in the same way that a [WMI query](/windows/desktop/WmiSdk/querying-wmi), such as `SELECT * from Win32_LogicalDisk`, returns a collection in an [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span></span> <span data-ttu-id="fed84-118">Para leer un archivo como una secuencia de texto, cree el objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) scripting y llame al método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para leer cada línea del archivo.</span><span class="sxs-lookup"><span data-stu-id="fed84-118">To read a file as a text stream, you create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="fed84-119">De forma similar, se llama al método **Session. Enumerate** para obtener un objeto de [**enumerador**](enumerator.md) y, a continuación, llamar al método **enumerador. ReadItem** .</span><span class="sxs-lookup"><span data-stu-id="fed84-119">In a similar way, you call the **Session.Enumerate** method to obtain an [**Enumerator**](enumerator.md) object and then call the **Enumerator.ReadItem** method.</span></span> <span data-ttu-id="fed84-120">Como en la lectura del archivo de texto, puede comprobar la propiedad [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) para comprobar si ha alcanzado el final de los elementos de datos.</span><span class="sxs-lookup"><span data-stu-id="fed84-120">As in reading from the text file, you can check the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

## <a name="examples"></a><span data-ttu-id="fed84-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fed84-121">Examples</span></span>

<span data-ttu-id="fed84-122">El siguiente ejemplo de VBScript llama al método [**Session. Enumerate**](session-enumerate.md) para obtener una lista de los trabajos programados.</span><span class="sxs-lookup"><span data-stu-id="fed84-122">The following VBScript example calls the [**Session.Enumerate**](session-enumerate.md) method to obtain a list of scheduled jobs.</span></span> <span data-ttu-id="fed84-123">La subrutina DisplayOutput usa el archivo de transformación XML de la herramienta de línea de comandos WinRM (WsmTxt. xsl) para generar los datos en un formato tabular.</span><span class="sxs-lookup"><span data-stu-id="fed84-123">The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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



## <a name="requirements"></a><span data-ttu-id="fed84-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fed84-124">Requirements</span></span>



| <span data-ttu-id="fed84-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed84-125">Requirement</span></span> | <span data-ttu-id="fed84-126">Value</span><span class="sxs-lookup"><span data-stu-id="fed84-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed84-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fed84-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fed84-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fed84-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fed84-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fed84-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fed84-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fed84-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fed84-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fed84-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fed84-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fed84-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fed84-133">IDL</span><span class="sxs-lookup"><span data-stu-id="fed84-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fed84-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fed84-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="fed84-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fed84-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fed84-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fed84-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fed84-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fed84-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fed84-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fed84-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fed84-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="fed84-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed84-140">**Enumerador**</span><span class="sxs-lookup"><span data-stu-id="fed84-140">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="fed84-141">Enumerar o enumerar todas las instancias de un recurso</span><span class="sxs-lookup"><span data-stu-id="fed84-141">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

