---
description: Asigna una cuota de disco no predeterminada a un nuevo usuario.
title: Método DiskQuotaControl.AddUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841536"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="5d033-103">Método DiskQuotaControl.AddUser</span><span class="sxs-lookup"><span data-stu-id="5d033-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="5d033-104">Asigna una cuota de disco no predeterminada a un nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="5d033-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d033-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d033-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="5d033-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d033-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="5d033-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="5d033-108">Tipo: **CHAR**</span><span class="sxs-lookup"><span data-stu-id="5d033-108">Type: **CHAR**</span></span>

<span data-ttu-id="5d033-109">Valor de cadena que contiene el nombre de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="5d033-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="5d033-110">Use la [**propiedad UserNameResolution**](diskquotacontrol-usernameresolution.md) para especificar cómo se va a resolver el nombre.</span><span class="sxs-lookup"><span data-stu-id="5d033-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d033-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d033-111">Return value</span></span>

<span data-ttu-id="5d033-112">Tipo: **Objeto**</span><span class="sxs-lookup"><span data-stu-id="5d033-112">Type: **Object**</span></span>

<span data-ttu-id="5d033-113">Devuelve una expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.</span><span class="sxs-lookup"><span data-stu-id="5d033-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d033-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d033-114">Remarks</span></span>

<span data-ttu-id="5d033-115">El sistema de archivos NTFS crea automáticamente una entrada de cuota de usuario cuando un usuario escribe por primera vez en el volumen.</span><span class="sxs-lookup"><span data-stu-id="5d033-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="5d033-116">A las entradas que se crean de esta manera se les asignan los valores predeterminados de umbral de advertencia y límite de cuota fija para el volumen.</span><span class="sxs-lookup"><span data-stu-id="5d033-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="5d033-117">Este método permite crear una entrada de cuota de usuario antes de que un usuario escriba información en el volumen.</span><span class="sxs-lookup"><span data-stu-id="5d033-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="5d033-118">Devuelve un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) que se puede usar para asignar un umbral de advertencia o un valor de límite de cuota que difiere de la configuración predeterminada del volumen.</span><span class="sxs-lookup"><span data-stu-id="5d033-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="5d033-119">Si el usuario ya existe, no se crea ninguna entrada nueva.</span><span class="sxs-lookup"><span data-stu-id="5d033-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="5d033-120">El método devuelve el [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) asociado a la entrada existente.</span><span class="sxs-lookup"><span data-stu-id="5d033-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d033-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d033-121">Requirements</span></span>



| <span data-ttu-id="5d033-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d033-122">Requirement</span></span> | <span data-ttu-id="5d033-123">Value</span><span class="sxs-lookup"><span data-stu-id="5d033-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d033-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d033-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d033-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d033-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d033-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d033-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d033-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d033-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5d033-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d033-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d033-129"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5d033-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d033-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5d033-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d033-131">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="5d033-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="5d033-132">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="5d033-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="5d033-133">**DiskQuotaControl (objeto)**</span><span class="sxs-lookup"><span data-stu-id="5d033-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




