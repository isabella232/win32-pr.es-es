---
description: Representa el encabezado de multisector.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Estructura de MULTI_SECTOR_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807063"
---
# <a name="multi_sector_header-structure"></a><span data-ttu-id="35ecb-103">Estructura de encabezado de varios \_ sectores \_</span><span class="sxs-lookup"><span data-stu-id="35ecb-103">MULTI\_SECTOR\_HEADER structure</span></span>

<span data-ttu-id="35ecb-104">\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]</span><span class="sxs-lookup"><span data-stu-id="35ecb-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="35ecb-105">Representa el encabezado de multisector.</span><span class="sxs-lookup"><span data-stu-id="35ecb-105">Represents the multisector header.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ecb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35ecb-106">Syntax</span></span>


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a><span data-ttu-id="35ecb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="35ecb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="35ecb-108">**Signature**</span><span class="sxs-lookup"><span data-stu-id="35ecb-108">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="35ecb-109">Signatura.</span><span class="sxs-lookup"><span data-stu-id="35ecb-109">The signature.</span></span> <span data-ttu-id="35ecb-110">Este valor es una comodidad para el usuario.</span><span class="sxs-lookup"><span data-stu-id="35ecb-110">This value is a convenience to the user.</span></span>

</dd> <dt>

<span data-ttu-id="35ecb-111">**UpdateSequenceArrayOffset**</span><span class="sxs-lookup"><span data-stu-id="35ecb-111">**UpdateSequenceArrayOffset**</span></span>
</dt> <dd>

<span data-ttu-id="35ecb-112">Desplazamiento de la matriz de secuencias de actualización, desde el principio de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="35ecb-112">The offset to the update sequence array, from the start of this structure.</span></span> <span data-ttu-id="35ecb-113">La matriz de secuencias de actualización debe finalizar antes del último valor USHORT en el primer sector.</span><span class="sxs-lookup"><span data-stu-id="35ecb-113">The update sequence array must end before the last USHORT value in the first sector.</span></span>

</dd> <dt>

<span data-ttu-id="35ecb-114">**UpdateSequenceArraySize**</span><span class="sxs-lookup"><span data-stu-id="35ecb-114">**UpdateSequenceArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="35ecb-115">Tamaño de la matriz de secuencias de actualización, en bytes.</span><span class="sxs-lookup"><span data-stu-id="35ecb-115">The size of the update sequence array, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35ecb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35ecb-116">Remarks</span></span>

<span data-ttu-id="35ecb-117">Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="35ecb-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="35ecb-118">Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="35ecb-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="35ecb-119">El encabezado multisector y la matriz de la secuencia de actualización proporcionan la detección de las transferencias de varios sectores incompletas para los dispositivos que tienen un tamaño de sector físico mayor o igual que el intervalo del número de secuencia (512) o que no transfieren los sectores fuera de orden.</span><span class="sxs-lookup"><span data-stu-id="35ecb-119">The multisector header and update sequence array provide detection of incomplete multisector transfers for devices that either have a physical sector size greater than or equal to the sequence number stride (512) or that do not transfer sectors out of order.</span></span> <span data-ttu-id="35ecb-120">Si existe un dispositivo que tiene un tamaño de sector menor que el intervalo del número de secuencia y, a veces, transfiere sectores de forma desordenada, la matriz de secuencias de actualización no proporcionará una detección absoluta de las transferencias incompletas.</span><span class="sxs-lookup"><span data-stu-id="35ecb-120">If a device exists that has a sector size smaller than the sequence number stride and it sometimes transfers sectors out of order, then the update sequence array will not provide absolute detection of incomplete transfers.</span></span> <span data-ttu-id="35ecb-121">El intervalo del número de secuencia se establece en un número lo suficientemente pequeño para proporcionar protección absoluta a todos los discos duros conocidos.</span><span class="sxs-lookup"><span data-stu-id="35ecb-121">The sequence number stride is set to a small enough number to provide absolute protection for all known hard disks.</span></span> <span data-ttu-id="35ecb-122">No se establece un valor menor o es posible que haya un tiempo de ejecución excesivo o una sobrecarga de espacio.</span><span class="sxs-lookup"><span data-stu-id="35ecb-122">It is not set any smaller or there might be excessive run time or space overhead.</span></span>

<span data-ttu-id="35ecb-123">La matriz de secuencias de actualización consta de una matriz de *n* valores **USHORT** , donde *n* es el tamaño de la estructura que se está protegiendo dividido por el intervalo del número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="35ecb-123">The update sequence array consists of an array of *n* **USHORT** values, where *n* is the size of the structure being protected divided by the sequence number stride.</span></span> <span data-ttu-id="35ecb-124">La primera palabra contiene el número de secuencia de actualización, que es un contador cíclico del número de veces que la estructura contenedora se ha escrito en el disco.</span><span class="sxs-lookup"><span data-stu-id="35ecb-124">The first word contains the update sequence number, which is a cyclical counter of the number of times the containing structure has been written to disk.</span></span> <span data-ttu-id="35ecb-125">A continuación se muestran los valores de **USHORT** *guardados que el número* de secuencia de actualización sobrescribió la última vez que la estructura contenedora se escribió en el disco.</span><span class="sxs-lookup"><span data-stu-id="35ecb-125">Next are the *n* saved **USHORT** values that were overwritten by the update sequence number the last time the containing structure was written to disk.</span></span>

<span data-ttu-id="35ecb-126">Cada vez que la estructura protegida está a punto de escribirse en el disco, la última palabra de cada intervalo del número de secuencia se guarda en su posición respectiva en la matriz del número de secuencia y, a continuación, se sobrescribe con el siguiente número de secuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="35ecb-126">Each time the protected structure is about to be written to disk, the last word in each sequence number stride is saved to its respective position in the sequence number array, then it is overwritten with the next update sequence number.</span></span> <span data-ttu-id="35ecb-127">Después de la escritura, o cada vez que se lee la estructura, la palabra guardada de la matriz del número de secuencia se restaura a su posición real en la estructura.</span><span class="sxs-lookup"><span data-stu-id="35ecb-127">After the write, or whenever the structure is read, the saved word from the sequence number array is restored to its actual position in the structure.</span></span> <span data-ttu-id="35ecb-128">Antes de restaurar las palabras guardadas en las lecturas, todos los números de secuencia al final de cada intervalo se comparan con el número de secuencia real al principio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="35ecb-128">Before restoring the saved words on reads, all the sequence numbers at the end of each stride are compared with the actual sequence number at the start of the array.</span></span> <span data-ttu-id="35ecb-129">Si alguna de estas comparaciones no es igual, se ha detectado una transferencia multisector con errores.</span><span class="sxs-lookup"><span data-stu-id="35ecb-129">If any of these comparisons are not equal, then a failed multisector transfer has been detected.</span></span>

<span data-ttu-id="35ecb-130">El tamaño de la matriz viene determinado por el tamaño de la estructura contenedora.</span><span class="sxs-lookup"><span data-stu-id="35ecb-130">The size of the array is determined by the size of the containing structure.</span></span> <span data-ttu-id="35ecb-131">La matriz de secuencias de actualización debe estar incluida al final del encabezado de la estructura que protege debido a su tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="35ecb-131">The update sequence array should be included at the end of the header of the structure it is protecting because of its variable size.</span></span> <span data-ttu-id="35ecb-132">El usuario debe asegurarse de que el espacio correcto está reservado para la estructura contenedora: (Size of Structure/512 + 1) \* sizeof (USHORT).</span><span class="sxs-lookup"><span data-stu-id="35ecb-132">The user must ensure that the correct space is reserved for the containing structure: (size of structure / 512 + 1) \* sizeof(USHORT).</span></span>

## <a name="see-also"></a><span data-ttu-id="35ecb-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ecb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ecb-134">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="35ecb-134">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
