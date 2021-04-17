---
description: Carga un certificado de firma desde un archivo. pfx especificado.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Signer. Load (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671235"
---
# <a name="signerload-method"></a><span data-ttu-id="76555-103">Signer. Load (método)</span><span class="sxs-lookup"><span data-stu-id="76555-103">Signer.Load method</span></span>

<span data-ttu-id="76555-104">\[El método **Load** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="76555-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="76555-105">En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="76555-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="76555-106">El método **Load** carga un certificado de firma desde un archivo. pfx especificado.</span><span class="sxs-lookup"><span data-stu-id="76555-106">The **Load** method loads a signing certificate from a specified .pfx file.</span></span>

## <a name="syntax"></a><span data-ttu-id="76555-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76555-107">Syntax</span></span>


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="76555-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76555-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76555-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="76555-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="76555-110">Nombre del archivo. pfx que contiene el certificado de firma.</span><span class="sxs-lookup"><span data-stu-id="76555-110">Name of the .pfx file that contains the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="76555-111">*Contraseña* \[ de opta\]</span><span class="sxs-lookup"><span data-stu-id="76555-111">*Password* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76555-112">Cadena que contiene la contraseña de texto no cifrado utilizada para abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="76555-112">String containing the plaintext password used to open the file.</span></span> <span data-ttu-id="76555-113">Se pueden usar hasta 32 caracteres Unicode, incluido un carácter nulo de terminación, para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="76555-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="76555-114">El valor predeterminado es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="76555-114">The default value is an empty string ("").</span></span> <span data-ttu-id="76555-115">Para obtener información acerca de cómo proteger la contraseña, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="76555-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76555-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76555-116">Return value</span></span>

<span data-ttu-id="76555-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="76555-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76555-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76555-118">Remarks</span></span>

<span data-ttu-id="76555-119">Este método carga el primer certificado en el archivo. pfx que tiene una clave privada asociada.</span><span class="sxs-lookup"><span data-stu-id="76555-119">This method loads the first certificate in the .pfx file that has a private key associated with it.</span></span>

<span data-ttu-id="76555-120">Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="76555-120">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="76555-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76555-121">Requirements</span></span>



| <span data-ttu-id="76555-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76555-122">Requirement</span></span> | <span data-ttu-id="76555-123">Value</span><span class="sxs-lookup"><span data-stu-id="76555-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76555-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="76555-124">Redistributable</span></span><br/> | <span data-ttu-id="76555-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="76555-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="76555-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="76555-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="76555-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76555-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76555-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="76555-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76555-129">**Firmante**</span><span class="sxs-lookup"><span data-stu-id="76555-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
