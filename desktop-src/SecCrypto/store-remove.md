---
description: El método Remove quita un certificado de un almacén de certificados abierto. Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670711"
---
# <a name="storeremove-method"></a><span data-ttu-id="4f8ed-104">Store. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="4f8ed-104">Store.Remove method</span></span>

<span data-ttu-id="4f8ed-105">\[El método **Remove** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-105">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4f8ed-106">En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4f8ed-106">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4f8ed-107">El método **Remove** quita un [*certificado*](../secgloss/c-gly.md) de un [*almacén de certificados*](../secgloss/c-gly.md)abierto.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-107">The **Remove** method removes a [*certificate*](../secgloss/c-gly.md) from an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="4f8ed-108">Este método solo se puede usar con un almacén que se ha abierto con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8ed-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f8ed-109">Syntax</span></span>


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="4f8ed-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f8ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f8ed-111">*Certificado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4f8ed-111">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8ed-112">Expresión que se resuelve como una instancia de un objeto de [**certificado**](certificate.md) que se va a quitar del almacén.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-112">Expression that resolves to an instance of a [**Certificate**](certificate.md) object to be removed from the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f8ed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f8ed-113">Return value</span></span>

<span data-ttu-id="4f8ed-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f8ed-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f8ed-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f8ed-116">Cuando se llama a este método desde un script Web, el script debe eliminar los certificados digitales del equipo local.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-116">When this method is called from a web script, the script needs to delete digital certificates from the local computer.</span></span> <span data-ttu-id="4f8ed-117">Permitir que los sitios web que no son de confianza eliminen los certificados digitales es un riesgo para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-117">Allowing untrusted websites to delete digital certificates is a security risk.</span></span> <span data-ttu-id="4f8ed-118">Un cuadro de diálogo que pregunta si el sitio web puede eliminar certificados aparece cuando se llama a este método por primera vez.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-118">A dialog box that asks whether the website can delete certificates appears when this method is first called.</span></span> <span data-ttu-id="4f8ed-119">Si permite que la aplicación elimine certificados y selecciona "no volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá para ningún script que elimine los certificados de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-119">If you allow the application to delete certificates and select "Do not show this dialog box again," the dialog box will no longer appear for any script that deletes certificates within that domain.</span></span> <span data-ttu-id="4f8ed-120">Sin embargo, los scripts que se encuentren fuera del dominio y que intenten eliminar certificados seguirán apareciendo este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-120">However, scripts outside that domain that attempt to delete certificates will still cause this dialog box to appear.</span></span> <span data-ttu-id="4f8ed-121">Si no permite que el script elimine certificados y selecciona "no volver a mostrar este cuadro de diálogo", se rechazará automáticamente la capacidad de eliminar certificados de los scripts dentro de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-121">If you do not allow the script to delete certificates and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to delete certificates.</span></span>

 

<span data-ttu-id="4f8ed-122">Al eliminar un certificado de un almacén, primero debe eliminar la clave privada asociada con el certificado.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-122">When you delete a certificate from a store, you should first delete the private key associated with the certificate.</span></span>

<span data-ttu-id="4f8ed-123">Si el almacén no está abierto con permiso de lectura y escritura, este método produce un error.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-123">If the store is not open with read/write permission, this method fails.</span></span> <span data-ttu-id="4f8ed-124">Aunque este método se puede utilizar con almacenes de memoria, los cambios realizados en un almacén de memoria no se conservan cuando se cierra el almacén.</span><span class="sxs-lookup"><span data-stu-id="4f8ed-124">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f8ed-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f8ed-125">Requirements</span></span>



| <span data-ttu-id="4f8ed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f8ed-126">Requirement</span></span> | <span data-ttu-id="4f8ed-127">Value</span><span class="sxs-lookup"><span data-stu-id="4f8ed-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8ed-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4f8ed-128">Redistributable</span></span><br/> | <span data-ttu-id="4f8ed-129">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f8ed-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4f8ed-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f8ed-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="4f8ed-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f8ed-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f8ed-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f8ed-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8ed-133">**Store**</span><span class="sxs-lookup"><span data-stu-id="4f8ed-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="4f8ed-134">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="4f8ed-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
