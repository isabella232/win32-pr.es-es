---
description: Agrega un objeto de certificado a un almacén de certificados abierto.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671233"
---
# <a name="storeadd-method"></a><span data-ttu-id="af228-103">Store. Add (método)</span><span class="sxs-lookup"><span data-stu-id="af228-103">Store.Add method</span></span>

<span data-ttu-id="af228-104">\[El método **Add** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="af228-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af228-105">En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="af228-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="af228-106">El método **Add** agrega un objeto de [**certificado**](certificate.md) a un [*almacén de certificados*](../secgloss/c-gly.md)abierto.</span><span class="sxs-lookup"><span data-stu-id="af228-106">The **Add** method adds a [**Certificate**](certificate.md) object to an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="af228-107">Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="af228-107">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="af228-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af228-108">Syntax</span></span>


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="af228-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af228-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af228-110">*Certificado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="af228-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af228-111">Expresión que se resuelve como un objeto de [**certificado**](certificate.md) que se va a agregar al almacén.</span><span class="sxs-lookup"><span data-stu-id="af228-111">Expression that resolves to a [**Certificate**](certificate.md) object to be added to the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af228-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af228-112">Return value</span></span>

<span data-ttu-id="af228-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="af228-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af228-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af228-114">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af228-115">Cuando se llama a este método en un almacén del sistema desde un script Web, el script debe tener acceso a los certificados digitales en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="af228-115">When this method is called on a system store from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="af228-116">Si permite que el script tenga acceso a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados.</span><span class="sxs-lookup"><span data-stu-id="af228-116">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="af228-117">La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados.</span><span class="sxs-lookup"><span data-stu-id="af228-117">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="af228-118">Si el almacén no está abierto en modo de lectura/escritura, este método produce un error.</span><span class="sxs-lookup"><span data-stu-id="af228-118">If the store is not open in read/write mode, this method fails.</span></span> <span data-ttu-id="af228-119">Aunque este método se puede utilizar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.</span><span class="sxs-lookup"><span data-stu-id="af228-119">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

<span data-ttu-id="af228-120">Si el certificado que se va a agregar al almacén es el mismo que el que ya existe, el método **Add** elimina el certificado existente del almacén y, a continuación, agrega el nuevo certificado.</span><span class="sxs-lookup"><span data-stu-id="af228-120">If the certificate being added to the store is the same as one that is already there, the **Add** method deletes the existing certificate from the store and then adds the new certificate.</span></span> <span data-ttu-id="af228-121">El nuevo certificado hereda las propiedades del certificado existente.</span><span class="sxs-lookup"><span data-stu-id="af228-121">The new certificate inherits properties from the existing certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="af228-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af228-122">Requirements</span></span>



| <span data-ttu-id="af228-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="af228-123">Requirement</span></span> | <span data-ttu-id="af228-124">Value</span><span class="sxs-lookup"><span data-stu-id="af228-124">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af228-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="af228-125">Redistributable</span></span><br/> | <span data-ttu-id="af228-126">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="af228-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="af228-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af228-127">DLL</span></span><br/>             | <dl> <span data-ttu-id="af228-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af228-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af228-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="af228-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af228-130">**Store**</span><span class="sxs-lookup"><span data-stu-id="af228-130">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="af228-131">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="af228-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
