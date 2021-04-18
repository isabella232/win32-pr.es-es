---
description: Carga el archivo de subárbol del registro especificado en la memoria y valida el subárbol.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Función OROpenHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671346"
---
# <a name="oropenhive-function"></a><span data-ttu-id="c9510-103">OROpenHive función)</span><span class="sxs-lookup"><span data-stu-id="c9510-103">OROpenHive function</span></span>

<span data-ttu-id="c9510-104">Carga el archivo de subárbol del registro especificado en la memoria y valida el subárbol.</span><span class="sxs-lookup"><span data-stu-id="c9510-104">Loads the specified registry hive file into memory and validates the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9510-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9510-105">Syntax</span></span>


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="c9510-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9510-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9510-107">*lpHivePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9510-107">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9510-108">Puntero a una cadena Unicode que especifica el nombre del archivo de subárbol del registro que se va a cargar en la memoria.</span><span class="sxs-lookup"><span data-stu-id="c9510-108">A pointer to a Unicode string that specifies the name of the registry hive file to be loaded into memory.</span></span> <span data-ttu-id="c9510-109">Puede tratarse de un archivo de Hive que se guardó con la función [**ORSaveHive**](orsavehive.md) o que se creó con la función [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) .</span><span class="sxs-lookup"><span data-stu-id="c9510-109">This can be a hive file that was saved with the [**ORSaveHive**](orsavehive.md) function or created with the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function.</span></span> <span data-ttu-id="c9510-110">El archivo debe tener un tamaño inferior a 4 GB y el llamador debe tener acceso de \_ datos de lectura de archivos \_ al archivo.</span><span class="sxs-lookup"><span data-stu-id="c9510-110">The file must be less than 4 GB in size, and the caller must have FILE\_READ\_DATA access to the file.</span></span> <span data-ttu-id="c9510-111">Para obtener más información, vea [seguridad de archivos y derechos de acceso](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="c9510-111">For more information, see [File Security and Access Rights](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9510-112">*phkResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9510-112">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9510-113">Un puntero a una variable que recibe un identificador a la clave raíz del subárbol del registro cargado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c9510-113">A pointer to a variable that receives a handle to the root key of the loaded offline registry hive.</span></span> <span data-ttu-id="c9510-114">Si no se puede abrir el archivo de subárbol del registro o se produce un error en la validación, la función establece este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="c9510-114">If the registry hive file cannot be opened or validation fails, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9510-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9510-115">Return value</span></span>

<span data-ttu-id="c9510-116">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c9510-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c9510-117">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="c9510-117">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="c9510-118">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="c9510-118">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="c9510-119">Entre los posibles códigos de error se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9510-119">Possible error codes include the following:</span></span>

-   <span data-ttu-id="c9510-120">Si el archivo está vacío o tiene un tamaño superior a 4 GB, la función devuelve el ERROR \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="c9510-120">If the file is empty or larger than 4 GB in size, the function returns ERROR\_BADDB.</span></span>
-   <span data-ttu-id="c9510-121">Si el llamador no tiene los derechos de acceso necesarios para abrir el archivo, la función devuelve el ERROR \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="c9510-121">If the caller does not have the necessary access rights to open the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="c9510-122">Si se produce un error en la validación del subárbol del registro, la función devuelve el ERROR \_ no \_ archivo de registro \_ .</span><span class="sxs-lookup"><span data-stu-id="c9510-122">If the registry hive fails validation, the function returns ERROR\_NOT\_REGISTRY\_FILE.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9510-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9510-123">Remarks</span></span>

<span data-ttu-id="c9510-124">La función **OROpenHive** es la única función de registro sin conexión que valida un subárbol del registro.</span><span class="sxs-lookup"><span data-stu-id="c9510-124">The **OROpenHive** function is the only offline registry function that validates a registry hive.</span></span> <span data-ttu-id="c9510-125">Si se produce un error en la validación, no se realiza ningún intento para reparar el subárbol.</span><span class="sxs-lookup"><span data-stu-id="c9510-125">If the validation fails, no attempt is made to repair the hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9510-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9510-126">Requirements</span></span>



| <span data-ttu-id="c9510-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9510-127">Requirement</span></span> | <span data-ttu-id="c9510-128">Value</span><span class="sxs-lookup"><span data-stu-id="c9510-128">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9510-129">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c9510-129">Redistributable</span></span><br/> | <span data-ttu-id="c9510-130">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c9510-130">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="c9510-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9510-131">Header</span></span><br/>          | <dl> <span data-ttu-id="c9510-132"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9510-132"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9510-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9510-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="c9510-134"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9510-134"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9510-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9510-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9510-136">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="c9510-136">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="c9510-137">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="c9510-137">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="c9510-138">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="c9510-138">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="c9510-139">RegSaveKey</span><span class="sxs-lookup"><span data-stu-id="c9510-139">RegSaveKey</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[<span data-ttu-id="c9510-140">RegSaveKeyEx</span><span class="sxs-lookup"><span data-stu-id="c9510-140">RegSaveKeyEx</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
