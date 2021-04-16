---
description: El método de importación copia en un certificado abierto almacena el contenido de un almacén de certificados exportado previamente. Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650017"
---
# <a name="storeimport-method"></a><span data-ttu-id="54d87-104">Store. Import (método)</span><span class="sxs-lookup"><span data-stu-id="54d87-104">Store.Import method</span></span>

<span data-ttu-id="54d87-105">\[El método de **importación** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="54d87-105">\[The **Import** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="54d87-106">En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="54d87-106">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="54d87-107">El método de **importación** copia en un [*certificado abierto almacena*](../secgloss/c-gly.md) el contenido de un almacén de certificados exportado previamente.</span><span class="sxs-lookup"><span data-stu-id="54d87-107">The **Import** method copies into an open [*certificate store*](../secgloss/c-gly.md) the contents of a previously exported certificate store.</span></span> <span data-ttu-id="54d87-108">Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="54d87-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d87-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54d87-109">Syntax</span></span>


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a><span data-ttu-id="54d87-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54d87-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d87-111">*EncodedStore* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54d87-111">*EncodedStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d87-112">Cadena que contiene los certificados codificados que se van a importar.</span><span class="sxs-lookup"><span data-stu-id="54d87-112">The string that contains the encoded certificates to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d87-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54d87-113">Return value</span></span>

<span data-ttu-id="54d87-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="54d87-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54d87-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54d87-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54d87-116">Cuando se llama a este método desde un script Web, el script debe tener acceso a los certificados digitales en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="54d87-116">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="54d87-117">Si permite que el script tenga acceso a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados.</span><span class="sxs-lookup"><span data-stu-id="54d87-117">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="54d87-118">La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados.</span><span class="sxs-lookup"><span data-stu-id="54d87-118">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="54d87-119">Si el almacén no se abre con permiso de lectura y escritura, este método produce un error.</span><span class="sxs-lookup"><span data-stu-id="54d87-119">If the store is not opened with read/write permission, this method fails.</span></span> <span data-ttu-id="54d87-120">Aunque este método se puede utilizar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.</span><span class="sxs-lookup"><span data-stu-id="54d87-120">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d87-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54d87-121">Requirements</span></span>



| <span data-ttu-id="54d87-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="54d87-122">Requirement</span></span> | <span data-ttu-id="54d87-123">Value</span><span class="sxs-lookup"><span data-stu-id="54d87-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54d87-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="54d87-124">Redistributable</span></span><br/> | <span data-ttu-id="54d87-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="54d87-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="54d87-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54d87-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="54d87-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54d87-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d87-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="54d87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d87-129">**Store**</span><span class="sxs-lookup"><span data-stu-id="54d87-129">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="54d87-130">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="54d87-130">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
