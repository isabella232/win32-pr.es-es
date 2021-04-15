---
description: La propiedad QualifierDescription de solo lectura devuelve una cadena de texto que describe el componente calificado.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Propiedad Installer. QualifierDescription
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653891"
---
# <a name="installerqualifierdescription-property"></a><span data-ttu-id="c8bf8-103">Propiedad Installer. QualifierDescription</span><span class="sxs-lookup"><span data-stu-id="c8bf8-103">Installer.QualifierDescription property</span></span>

<span data-ttu-id="c8bf8-104">La propiedad **QualifierDescription** de solo lectura devuelve una cadena de texto que describe el componente calificado.</span><span class="sxs-lookup"><span data-stu-id="c8bf8-104">The read-only **QualifierDescription** property returns a text string describing the qualified component.</span></span> <span data-ttu-id="c8bf8-105">Esta cadena traducible se crea en la columna AppData de la [tabla PublishComponent](publishcomponent-table.md) y se puede mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="c8bf8-105">This localizable string is authored into the AppData column of the [PublishComponent table](publishcomponent-table.md) and can be displayed to the user.</span></span> <span data-ttu-id="c8bf8-106">El calificador distingue varias formas del mismo componente, como un componente que se implementa en varios lenguajes.</span><span class="sxs-lookup"><span data-stu-id="c8bf8-106">The qualifier distinguishes multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span>

<span data-ttu-id="c8bf8-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c8bf8-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bf8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8bf8-108">Syntax</span></span>


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a><span data-ttu-id="c8bf8-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c8bf8-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c8bf8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8bf8-110">Requirements</span></span>



| <span data-ttu-id="c8bf8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8bf8-111">Requirement</span></span> | <span data-ttu-id="c8bf8-112">Value</span><span class="sxs-lookup"><span data-stu-id="c8bf8-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bf8-113">Versión</span><span class="sxs-lookup"><span data-stu-id="c8bf8-113">Version</span></span><br/> | <span data-ttu-id="c8bf8-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8bf8-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c8bf8-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8bf8-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c8bf8-116">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8bf8-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c8bf8-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8bf8-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8bf8-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8bf8-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c8bf8-119">IID</span><span class="sxs-lookup"><span data-stu-id="c8bf8-119">IID</span></span><br/>     | <span data-ttu-id="c8bf8-120">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c8bf8-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c8bf8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8bf8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bf8-122">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="c8bf8-122">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[<span data-ttu-id="c8bf8-123">Componentes completos</span><span class="sxs-lookup"><span data-stu-id="c8bf8-123">Qualified Components</span></span>](qualified-components.md)
</dt> </dl>

 

 




