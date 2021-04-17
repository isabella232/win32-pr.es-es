---
description: 'Más información acerca de: estructura de JET_LOGINFO'
title: Estructura de JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105698462"
---
# <a name="jet_loginfo-structure"></a><span data-ttu-id="18c5f-103">Estructura de JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="18c5f-103">JET_LOGINFO Structure</span></span>


<span data-ttu-id="18c5f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="18c5f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_loginfo-structure"></a><span data-ttu-id="18c5f-105">Estructura de JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="18c5f-105">JET_LOGINFO Structure</span></span>

<span data-ttu-id="18c5f-106">La estructura **JET_LOGINFO** devuelve información estructurada sobre el conjunto de archivos de registro de transacciones que debe formar parte de un conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="18c5f-106">The **JET_LOGINFO** structure returns structured information about the set of transaction log files that should be a part of a backup file set.</span></span> <span data-ttu-id="18c5f-107">La estructura **JET_LOGINFO** es el conjunto mínimo de información necesaria para representar un intervalo de registros que se recupera con [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) o que se especifica para una recuperación de hardware con [JetExternalRestore2](./jetexternalrestore2-function.md).</span><span class="sxs-lookup"><span data-stu-id="18c5f-107">The **JET_LOGINFO** structure is the minimal set of information needed to represent a range of logs that is retrieved with [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) or specified for a hard recovery with [JetExternalRestore2](./jetexternalrestore2-function.md).</span></span>

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a><span data-ttu-id="18c5f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="18c5f-108">Members</span></span>

<span data-ttu-id="18c5f-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="18c5f-109">**cbSize**</span></span>

<span data-ttu-id="18c5f-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="18c5f-110">The size of the structure, in bytes.</span></span>

<span data-ttu-id="18c5f-111">Este miembro permite la expansión futura de esta estructura mientras se habilita la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="18c5f-111">This member enables future expansion of this structure while enabling backwards compatibility.</span></span> <span data-ttu-id="18c5f-112">Siempre debe establecerse en sizeof (JET_LOGINFO).</span><span class="sxs-lookup"><span data-stu-id="18c5f-112">It should always be set to sizeof( JET_LOGINFO ).</span></span>

<span data-ttu-id="18c5f-113">**ulGenLow**</span><span class="sxs-lookup"><span data-stu-id="18c5f-113">**ulGenLow**</span></span>

<span data-ttu-id="18c5f-114">El número de archivo de registro más bajo (o más antiguo) que se restaura.</span><span class="sxs-lookup"><span data-stu-id="18c5f-114">The lowest (or oldest) log file number that is restored.</span></span> <span data-ttu-id="18c5f-115">Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="18c5f-115">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="18c5f-116">Esto podría cambiar en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="18c5f-116">This might change in future versions.</span></span>

<span data-ttu-id="18c5f-117">**ulGenHigh**</span><span class="sxs-lookup"><span data-stu-id="18c5f-117">**ulGenHigh**</span></span>

<span data-ttu-id="18c5f-118">El número de archivo de registro más alto (o más reciente) que se restaura.</span><span class="sxs-lookup"><span data-stu-id="18c5f-118">The highest (or most recent) log file number that is restored.</span></span> <span data-ttu-id="18c5f-119">Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="18c5f-119">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="18c5f-120">Esto podría cambiar en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="18c5f-120">This might change in future versions.</span></span>

<span data-ttu-id="18c5f-121">**szBaseName**</span><span class="sxs-lookup"><span data-stu-id="18c5f-121">**szBaseName**</span></span>

<span data-ttu-id="18c5f-122">El prefijo usado para asignar un nombre a los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="18c5f-122">The prefix used to name the transaction log files.</span></span>

<span data-ttu-id="18c5f-123">El valor que se devuelve en este miembro siempre es igual al valor de [JET_paramBaseName](./transaction-log-parameters.md) para la instancia que generó esta información.</span><span class="sxs-lookup"><span data-stu-id="18c5f-123">The value that is returned in this member is always equal to the setting for [JET_paramBaseName](./transaction-log-parameters.md) for the instance that generated this information.</span></span>

### <a name="remarks"></a><span data-ttu-id="18c5f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18c5f-124">Remarks</span></span>

<span data-ttu-id="18c5f-125">Los archivos de registro de transacciones se denominan según el nombre base de la instancia y el número de generación del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="18c5f-125">Transaction log files are named according to the instance base name and the generation number of the log file.</span></span> <span data-ttu-id="18c5f-126">El nombre tiene el formato BBBXXXXX. Inicia.</span><span class="sxs-lookup"><span data-stu-id="18c5f-126">The name is of the format BBBXXXXX.LOG.</span></span> <span data-ttu-id="18c5f-127">BBB corresponde al nombre base del archivo de registro y tiene siempre tres caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="18c5f-127">BBB corresponds to the base name for the log file and is always three characters in length.</span></span> <span data-ttu-id="18c5f-128">XXXXX corresponde al número de generación del archivo de registro en un valor hexadecimal con ceros rellenado y siempre tiene cinco caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="18c5f-128">XXXXX corresponds to the generation number of the log file in zero padded hexadecimal and is always five characters in length.</span></span> <span data-ttu-id="18c5f-129">LOG es la extensión de archivo que el motor siempre proporciona a los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="18c5f-129">LOG is the file extension that is always given to transaction log files by the engine.</span></span>

<span data-ttu-id="18c5f-130">No se recomienda el uso de esta información estructurada porque hace que la aplicación tenga un conocimiento profundo de este esquema de nomenclatura para los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="18c5f-130">Use of this structured information is discouraged because it causes the application to have intimate knowledge of this naming scheme for transaction log files.</span></span> <span data-ttu-id="18c5f-131">Si el esquema de nombres cambia alguna vez en el futuro, este tipo de aplicación dejará de funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="18c5f-131">If the naming scheme ever changes in the future then such an application will no longer function properly.</span></span> <span data-ttu-id="18c5f-132">Es imaginable que el formato del registro cambie para incorporar 8 dígitos hexadecimales en el futuro.</span><span class="sxs-lookup"><span data-stu-id="18c5f-132">It is conceivable that the log format will change to incorporate 8 hex digits in the future.</span></span> <span data-ttu-id="18c5f-133">En su lugar, las aplicaciones deben utilizar la lista explícita de nombres de archivo devueltos por [JetGetLogInfo](./jetgetloginfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="18c5f-133">Applications should use the explicit list of file names returned by [JetGetLogInfo](./jetgetloginfo-function.md) instead.</span></span>

### <a name="requirements"></a><span data-ttu-id="18c5f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18c5f-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c5f-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="18c5f-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18c5f-136">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18c5f-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c5f-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="18c5f-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18c5f-138">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="18c5f-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c5f-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="18c5f-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18c5f-140">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="18c5f-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c5f-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="18c5f-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="18c5f-142">Se implementa como <strong>JET_LOGINFO_W</strong> (Unicode) y <strong>JET_LOGINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="18c5f-142">Implemented as <strong>JET_LOGINFO_W</strong> (Unicode) and <strong>JET_LOGINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="18c5f-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="18c5f-143">See Also</span></span>

[<span data-ttu-id="18c5f-144">JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="18c5f-144">JetExternalRestore2</span></span>](./jetexternalrestore2-function.md)  
[<span data-ttu-id="18c5f-145">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="18c5f-145">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="18c5f-146">JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="18c5f-146">JetGetLogInfoInstance2</span></span>](./jetgetloginfoinstance2-function.md)  
[<span data-ttu-id="18c5f-147">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="18c5f-147">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
