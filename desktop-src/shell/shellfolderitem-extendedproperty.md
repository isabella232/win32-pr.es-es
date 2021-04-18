---
description: Obtiene el valor de una propiedad del conjunto de propiedades de un elemento. La propiedad se puede especificar por nombre o por el identificador de formato del conjunto de propiedades (FMTID) y el identificador de propiedad (PID).
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Método ShellFolderItem. ExtendedProperty (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985879"
---
# <a name="shellfolderitemextendedproperty-method"></a><span data-ttu-id="dd12e-104">ShellFolderItem. ExtendedProperty, método</span><span class="sxs-lookup"><span data-stu-id="dd12e-104">ShellFolderItem.ExtendedProperty method</span></span>

<span data-ttu-id="dd12e-105">Obtiene el valor de una propiedad del conjunto de propiedades de un elemento.</span><span class="sxs-lookup"><span data-stu-id="dd12e-105">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="dd12e-106">La propiedad se puede especificar por nombre o por el identificador de formato del conjunto de propiedades (FMTID) y el identificador de propiedad (PID).</span><span class="sxs-lookup"><span data-stu-id="dd12e-106">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd12e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd12e-107">Syntax</span></span>


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a><span data-ttu-id="dd12e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd12e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd12e-109">*sPropName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd12e-109">*sPropName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd12e-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="dd12e-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="dd12e-111">Valor de **cadena** que especifica la propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd12e-111">A **String** value that specifies the property.</span></span> <span data-ttu-id="dd12e-112">Para obtener información detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="dd12e-112">See the Remarks section for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd12e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd12e-113">Return value</span></span>

<span data-ttu-id="dd12e-114">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="dd12e-114">Type: \**Variant\** _</span></span>

<span data-ttu-id="dd12e-115">Cuando este método devuelve un valor, contiene el valor de la propiedad, si existe para el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="dd12e-115">When this method returns, contains the value of the property, if it exists for the specified item.</span></span> <span data-ttu-id="dd12e-116">El valor tendrá tipos completos; por ejemplo, las fechas se devuelven como fechas, no como cadenas.</span><span class="sxs-lookup"><span data-stu-id="dd12e-116">The value will have full typing—for example, dates are returned as dates, not strings.</span></span>

<span data-ttu-id="dd12e-117">Este método devuelve una cadena de longitud cero si la propiedad es válida pero no existe para el elemento especificado o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dd12e-117">This method returns a zero-length string if the property is valid but does not exist for the specified item, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd12e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd12e-118">Remarks</span></span>

<span data-ttu-id="dd12e-119">Hay dos maneras de especificar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd12e-119">There are two ways to specify a property.</span></span> <span data-ttu-id="dd12e-120">La primera es asignar el nombre conocido de la propiedad, como "autor" o "fecha", para _sPropName \*.</span><span class="sxs-lookup"><span data-stu-id="dd12e-120">The first is to assign the property's well-known name, such as "Author" or "Date", to _sPropName\*.</span></span> <span data-ttu-id="dd12e-121">Sin embargo, cada propiedad es un miembro de un conjunto de propiedades del modelo de objetos componentes (COM) y también se puede identificar especificando su identificador de formato (FMTID) y el identificador de propiedad (PID).</span><span class="sxs-lookup"><span data-stu-id="dd12e-121">However, each property is a member of a Component Object Model (COM) property set and can also be identified by specifying its format ID (FMTID) and property ID (PID).</span></span> <span data-ttu-id="dd12e-122">Un [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) es un GUID que identifica el conjunto de propiedades y un [**PID**](../stg/structured-storage-serialized-property-set-format.md) es un entero que identifica una propiedad determinada dentro del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd12e-122">An [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) is a GUID that identifies the property set, and a [**PID**](../stg/structured-storage-serialized-property-set-format.md) is an integer that identifies a particular property within the property set.</span></span>

<span data-ttu-id="dd12e-123">Especificar una propiedad por sus valores FMTID/PID suele ser más eficaz que usar su nombre.</span><span class="sxs-lookup"><span data-stu-id="dd12e-123">Specifying a property by its FMTID/PID values is usually more efficient than using its name.</span></span> <span data-ttu-id="dd12e-124">Para usar los valores de FMTID/PID de una propiedad con **ExtendedProperty**, deben combinarse en SCID.</span><span class="sxs-lookup"><span data-stu-id="dd12e-124">To use a property's FMTID/PID values with **ExtendedProperty**, they must be combined into an SCID.</span></span> <span data-ttu-id="dd12e-125">SCID es una cadena que contiene los valores de FMTID/PID con el formato "*FMTID \* \* PID*", donde FMTID es la forma de cadena del GUID del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd12e-125">An SCID is a string that contains the FMTID/PID values in the form "*FMTID\*\*PID*", where the FMTID is the string form of the property set's GUID.</span></span> <span data-ttu-id="dd12e-126">Por ejemplo, el SCID de la propiedad de autor del conjunto de propiedades de información de resumen es "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span><span class="sxs-lookup"><span data-stu-id="dd12e-126">For example, the SCID of the summary information property set's author property is "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span></span>

<span data-ttu-id="dd12e-127">Para obtener una lista de los FMTIDs y los PID actualmente admitidos por el Shell, consulte [**SHCOLUMNID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="dd12e-127">For a list of FMTIDs and PIDs that are currently supported by the Shell, see [**SHCOLUMNID**](./objects.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dd12e-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dd12e-128">Examples</span></span>

<span data-ttu-id="dd12e-129">En este código de ejemplo se muestra cómo usar **ExtendedProperty** para recuperar las propiedades "title" y "author" de un documento de Word.</span><span class="sxs-lookup"><span data-stu-id="dd12e-129">This sample code illustrates how to use **ExtendedProperty** to retrieve the "Title" and "Author" properties from a Word document.</span></span> <span data-ttu-id="dd12e-130">Una vez que tenga el objeto [**ShellFolderItem**](shellfolderitem-object.md) asociado al archivo, *fiWordDoc* en este ejemplo, recupere el valor de la propiedad pasando su nombre a **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="dd12e-130">Once you have the [**ShellFolderItem**](shellfolderitem-object.md) object associated with the file, *fiWordDoc* in this example, retrieve the property's value by passing its name to **ExtendedProperty**.</span></span>


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



<span data-ttu-id="dd12e-131">Un enfoque más rápido y eficaz consiste en pasar un SCID a **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="dd12e-131">A faster and more efficient approach is to pass an SCID to **ExtendedProperty**.</span></span>


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



<span data-ttu-id="dd12e-132">En los siguientes ejemplos se muestra el uso correcto de este método para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dd12e-132">The following examples show the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dd12e-133">JScript.net</span><span class="sxs-lookup"><span data-stu-id="dd12e-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="dd12e-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="dd12e-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="dd12e-135">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dd12e-135">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dd12e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd12e-136">Requirements</span></span>



| <span data-ttu-id="dd12e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd12e-137">Requirement</span></span> | <span data-ttu-id="dd12e-138">Value</span><span class="sxs-lookup"><span data-stu-id="dd12e-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd12e-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd12e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dd12e-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dd12e-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd12e-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd12e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dd12e-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd12e-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dd12e-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd12e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd12e-144"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd12e-144"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="dd12e-145">IDL</span><span class="sxs-lookup"><span data-stu-id="dd12e-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd12e-146"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd12e-146"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="dd12e-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd12e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd12e-148"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dd12e-148"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
