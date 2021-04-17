---
description: Crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: SignedCode. Sign (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690757"
---
# <a name="signedcodesign-method"></a><span data-ttu-id="8b7ee-103">SignedCode. Sign (método)</span><span class="sxs-lookup"><span data-stu-id="8b7ee-103">SignedCode.Sign method</span></span>

<span data-ttu-id="8b7ee-104">\[El método **Sign** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-104">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8b7ee-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="8b7ee-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="8b7ee-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="8b7ee-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="8b7ee-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="8b7ee-108">El método **Sign** crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="8b7ee-108">The **Sign** method creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7ee-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b7ee-109">Syntax</span></span>


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8b7ee-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b7ee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b7ee-111">*Firmante* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8b7ee-111">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7ee-112">Objeto de [**firmante**](signer.md) que tiene acceso a la clave privada del certificado utilizado para firmar el código.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-112">A [**Signer**](signer.md) object that has access to the private key of the certificate used to sign the code.</span></span> <span data-ttu-id="8b7ee-113">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-113">The default value is **Null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b7ee-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b7ee-114">Return value</span></span>

<span data-ttu-id="8b7ee-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b7ee-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b7ee-116">Remarks</span></span>

<span data-ttu-id="8b7ee-117">Antes de llamar al método **Sign** , el archivo que contiene el código debe especificarse en la propiedad [**filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="8b7ee-117">Before the **Sign** method is called, the file that contains the code must be specified in the [**FileName**](signedcode-filename.md) property.</span></span>

<span data-ttu-id="8b7ee-118">Si el archivo ejecutable ya está firmado, este método sobrescribe la firma existente.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-118">If the executable file is already signed, this method overwrites the existing signature.</span></span>

<span data-ttu-id="8b7ee-119">Los resultados siguientes se aplican al valor del parámetro *Signer* :</span><span class="sxs-lookup"><span data-stu-id="8b7ee-119">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="8b7ee-120">Si el parámetro del *firmante* no es **null**, este método utiliza la clave privada a la que apunta el certificado asociado para cifrar la firma.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-120">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="8b7ee-121">Si no está disponible la clave privada a la que apunta el certificado, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-121">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="8b7ee-122">Si el parámetro de *firmante* es **null** y hay exactamente un certificado en el usuario actual \_ mi almacén que tiene acceso a una clave privada con la funcionalidad de firma de código, ese certificado se usa para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-122">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key with code signing capability, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="8b7ee-123">Si el parámetro de *firmante* es **null**, el valor de la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es true y hay más de un certificado en el \_ usuario actual My Store con una clave privada disponible con la funcionalidad de firma de código, aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se usa.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-123">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key with code signing capability, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="8b7ee-124">Si el parámetro de *firmante* es **null** y la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-124">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="8b7ee-125">Si el parámetro del *firmante* es **null** y no hay ningún certificado en el \_ almacén del usuario actual con una clave privada disponible con la funcionalidad de firma de código, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-125">If the *Signer* parameter is **NULL** and there are no certificates in the CURRENT\_USER MY store with an available private key with code signing capability, the method fails.</span></span>

<span data-ttu-id="8b7ee-126">Este método usa el algoritmo hash SHA-1.</span><span class="sxs-lookup"><span data-stu-id="8b7ee-126">This method uses the SHA-1 hashing algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b7ee-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b7ee-127">Requirements</span></span>



| <span data-ttu-id="8b7ee-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b7ee-128">Requirement</span></span> | <span data-ttu-id="8b7ee-129">Value</span><span class="sxs-lookup"><span data-stu-id="8b7ee-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7ee-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8b7ee-130">Redistributable</span></span><br/> | <span data-ttu-id="8b7ee-131">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="8b7ee-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8b7ee-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b7ee-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="8b7ee-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b7ee-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
