---
description: La propiedad ProductElevated del objeto de instalador devuelve true si el producto está administrado o false si el producto no está administrado.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Instalador::P propiedad roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653957"
---
# <a name="installerproductelevated-property"></a><span data-ttu-id="a427a-103">Instalador::P propiedad roductElevated</span><span class="sxs-lookup"><span data-stu-id="a427a-103">Installer::ProductElevated property</span></span>

<span data-ttu-id="a427a-104">La propiedad **ProductElevated** del objeto de [**instalador**](installer-object.md) devuelve true si el producto está administrado o false si el producto no está administrado.</span><span class="sxs-lookup"><span data-stu-id="a427a-104">The **ProductElevated** property of the [**Installer**](installer-object.md) object returns True if the product is managed or False if the product is not managed.</span></span>

<span data-ttu-id="a427a-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a427a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a427a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a427a-106">Syntax</span></span>


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a><span data-ttu-id="a427a-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a427a-107">Property value</span></span>

<span data-ttu-id="a427a-108">El GUID completo del código del producto.</span><span class="sxs-lookup"><span data-stu-id="a427a-108">The full product code GUID of the product.</span></span> <span data-ttu-id="a427a-109">Este parámetro es necesario.</span><span class="sxs-lookup"><span data-stu-id="a427a-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="a427a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a427a-110">Remarks</span></span>

<span data-ttu-id="a427a-111">La propiedad **ProductElevated** usa la función [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) .</span><span class="sxs-lookup"><span data-stu-id="a427a-111">The **ProductElevated** property uses the [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) function.</span></span> <span data-ttu-id="a427a-112">El valor devuelto de la propiedad no tiene en cuenta la directiva [AlwaysInstallElevated](alwaysinstallelevated.md) .</span><span class="sxs-lookup"><span data-stu-id="a427a-112">The return of the property does not take into account the [AlwaysInstallElevated](alwaysinstallelevated.md) policy.</span></span>

## <a name="examples"></a><span data-ttu-id="a427a-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a427a-113">Examples</span></span>

<span data-ttu-id="a427a-114">En el siguiente script de ejemplo se muestra el uso de la propiedad **ProductElevated** .</span><span class="sxs-lookup"><span data-stu-id="a427a-114">The following sample script demonstrates the use of the **ProductElevated** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a><span data-ttu-id="a427a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a427a-115">Requirements</span></span>



| <span data-ttu-id="a427a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a427a-116">Requirement</span></span> | <span data-ttu-id="a427a-117">Value</span><span class="sxs-lookup"><span data-stu-id="a427a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a427a-118">Versión</span><span class="sxs-lookup"><span data-stu-id="a427a-118">Version</span></span><br/> | <span data-ttu-id="a427a-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a427a-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a427a-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a427a-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a427a-121">Windows Installer 4,5 en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a427a-121">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="a427a-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a427a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="a427a-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a427a-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="a427a-124">IID</span><span class="sxs-lookup"><span data-stu-id="a427a-124">IID</span></span><br/>     | <span data-ttu-id="a427a-125">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a427a-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="a427a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a427a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a427a-127">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="a427a-127">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="a427a-128">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="a427a-128">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




