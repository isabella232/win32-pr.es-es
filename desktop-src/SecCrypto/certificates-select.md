---
description: Muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de los certificados seleccionados.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'ICertificates2:: SELECT (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691019"
---
# <a name="icertificates2select-method"></a><span data-ttu-id="3aa37-103">ICertificates2:: SELECT (método)</span><span class="sxs-lookup"><span data-stu-id="3aa37-103">ICertificates2::Select method</span></span>

<span data-ttu-id="3aa37-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3aa37-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3aa37-105">En su lugar, use la [**clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3aa37-106">El método **Select** muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de los certificados seleccionados.</span><span class="sxs-lookup"><span data-stu-id="3aa37-106">The **Select** method displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span> <span data-ttu-id="3aa37-107">Este método se presentó en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="3aa37-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa37-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3aa37-108">Syntax</span></span>


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3aa37-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3aa37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa37-110">*Título* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-110">*Title* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-111">Cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3aa37-111">String that contains the title for the dialog box.</span></span> <span data-ttu-id="3aa37-112">El valor predeterminado es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="3aa37-112">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-113">*DisplayString* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-113">*DisplayString* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-114">Cadena que contiene el texto del mensaje que se muestra con el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3aa37-114">String that contains the prompt text displayed with the dialog box.</span></span> <span data-ttu-id="3aa37-115">El valor predeterminado es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="3aa37-115">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="3aa37-116">*bMultiSelect* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3aa37-116">*bMultiSelect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa37-117">Valor booleano que indica si el usuario puede seleccionar más de un certificado.</span><span class="sxs-lookup"><span data-stu-id="3aa37-117">Boolean value that indicates whether the user can select more than one certificate.</span></span> <span data-ttu-id="3aa37-118">True indica que se pueden seleccionar varios certificados mediante la tecla CTRL o Mayús.</span><span class="sxs-lookup"><span data-stu-id="3aa37-118">True indicates multiple certificates can be selected by using the CTRL or SHIFT key.</span></span> <span data-ttu-id="3aa37-119">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="3aa37-119">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa37-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3aa37-120">Return value</span></span>

<span data-ttu-id="3aa37-121">Objeto de [**certificados**](certificates.md) que contiene los certificados seleccionados en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3aa37-121">A [**Certificates**](certificates.md) object that contains the certificates selected from the dialog box.</span></span>

<span data-ttu-id="3aa37-122">**CAPICOM 2,1:** El objeto de [**certificados**](certificates.md) que se devuelve contiene referencias a los certificados de la colección de la que se realizó la selección.</span><span class="sxs-lookup"><span data-stu-id="3aa37-122">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="3aa37-123">Cualquier cambio realizado en los certificados del objeto de **certificados** devueltos se refleja en esa colección.</span><span class="sxs-lookup"><span data-stu-id="3aa37-123">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="3aa37-124">**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 y CAPICOM 2.0.0.3:** El objeto de [**certificados**](certificates.md) que se devuelve contiene copias de los certificados de la colección de la que se realizó la selección.</span><span class="sxs-lookup"><span data-stu-id="3aa37-124">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="3aa37-125">Los cambios realizados en los certificados del objeto de **certificados** devueltos no se reflejan en esa colección.</span><span class="sxs-lookup"><span data-stu-id="3aa37-125">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa37-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa37-126">Requirements</span></span>



| <span data-ttu-id="3aa37-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa37-127">Requirement</span></span> | <span data-ttu-id="3aa37-128">Value</span><span class="sxs-lookup"><span data-stu-id="3aa37-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa37-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3aa37-129">End of client support</span></span><br/> | <span data-ttu-id="3aa37-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3aa37-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3aa37-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3aa37-131">End of server support</span></span><br/> | <span data-ttu-id="3aa37-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aa37-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3aa37-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3aa37-133">Redistributable</span></span><br/>       | <span data-ttu-id="3aa37-134">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3aa37-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3aa37-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3aa37-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3aa37-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aa37-136"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
