---
description: El método transfer del objeto Item transfiere datos de un dispositivo a un archivo. Este método solo se aplica a los elementos de tipo de dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696617"
---
# <a name="itemtransfer-method"></a><span data-ttu-id="dced6-104">Item. Transfer (método)</span><span class="sxs-lookup"><span data-stu-id="dced6-104">Item.Transfer method</span></span>

<span data-ttu-id="dced6-105">El método **Transfer** del objeto [**Item**](-wia-item.md) transfiere datos de un dispositivo a un archivo.</span><span class="sxs-lookup"><span data-stu-id="dced6-105">The **Transfer** method of the [**Item**](-wia-item.md) object transfers data from a device to a file.</span></span> <span data-ttu-id="dced6-106">Este método solo se aplica a los elementos de tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dced6-106">This method applies only to device type items.</span></span>

## <a name="syntax"></a><span data-ttu-id="dced6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dced6-107">Syntax</span></span>


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a><span data-ttu-id="dced6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dced6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dced6-109">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dced6-109">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced6-110">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dced6-110">Type: **BSTR**</span></span>

<span data-ttu-id="dced6-111">Especifica el nombre del archivo al que se transfieren los datos.</span><span class="sxs-lookup"><span data-stu-id="dced6-111">Specifies the name of the file to which the data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="dced6-112">*AsyncTransfer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dced6-112">*AsyncTransfer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dced6-113">Tipo: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="dced6-113">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="dced6-114">Valor booleano que especifica si la transferencia se debe ejecutar como una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="dced6-114">A Boolean value that specifies whether the transfer should be run as an asynchronous call.</span></span>

<dt>



 <span data-ttu-id="dced6-115">(Variante \_ BOOLEANO</span><span class="sxs-lookup"><span data-stu-id="dced6-115">(VARIANT\_BOOL)</span></span>


</dt> <dd>

<span data-ttu-id="dced6-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dced6-116">Default.</span></span> <span data-ttu-id="dced6-117">Establezca este valor en **true** si la llamada debe ser asincrónica (vea la **sección Comentarios**).</span><span class="sxs-lookup"><span data-stu-id="dced6-117">Set this value to **true** if the call should be asynchronous (see **Remarks**).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dced6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dced6-118">Return value</span></span>

<span data-ttu-id="dced6-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dced6-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dced6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dced6-120">Remarks</span></span>

<span data-ttu-id="dced6-121">Este método solo se aplica a los elementos de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="dced6-121">This method applies only to file type items.</span></span> <span data-ttu-id="dced6-122">El método comprueba que el elemento admite este método antes de intentar completar la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="dced6-122">The method checks that the item supports this method before it attempts to complete the data transfer.</span></span>

<span data-ttu-id="dced6-123">Use "Clipboard" como parámetro *filename* para transferir un elemento al portapapeles.</span><span class="sxs-lookup"><span data-stu-id="dced6-123">Use "clipboard" as the *Filename* parameter to transfer an item to the clipboard.</span></span>

<span data-ttu-id="dced6-124">Establezca el valor de *AsyncTransfer* en **false** para las transferencias de cualquier aplicación o script que se ejecute en un entorno que termine un proceso al final de un script, como Windows Script Host (WSH).</span><span class="sxs-lookup"><span data-stu-id="dced6-124">Set the *AsyncTransfer* value to **false** for transfers within any application or script that runs in an environment that terminates a process at the end of a script, such as Windows Script Host (WSH).</span></span> <span data-ttu-id="dced6-125">De lo contrario, el script puede finalizar y el proceso finaliza antes de que se complete la transferencia.</span><span class="sxs-lookup"><span data-stu-id="dced6-125">Otherwise, the script may end, and the process terminate, before the transfer completes.</span></span>

<span data-ttu-id="dced6-126">El método **Transfer** no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="dced6-126">The **Transfer** method has no return value.</span></span> <span data-ttu-id="dced6-127">Tras la finalización de una transferencia, este método envía un evento [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) al script o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dced6-127">Upon completion of a transfer, this method sends an [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) event to the script or application.</span></span>

## <a name="examples"></a><span data-ttu-id="dced6-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dced6-128">Examples</span></span>

<span data-ttu-id="dced6-129">En el siguiente ejemplo se muestra el uso del método **Transfer** para transferir datos desde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dced6-129">The following example demonstrates the use of the **Transfer** method to transfer data from a device.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="dced6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dced6-130">Requirements</span></span>



| <span data-ttu-id="dced6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dced6-131">Requirement</span></span> | <span data-ttu-id="dced6-132">Value</span><span class="sxs-lookup"><span data-stu-id="dced6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dced6-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dced6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dced6-134">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dced6-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dced6-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dced6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dced6-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dced6-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dced6-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dced6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dced6-138"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dced6-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




