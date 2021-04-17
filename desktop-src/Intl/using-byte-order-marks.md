---
description: Prefije siempre un archivo de texto sin formato Unicode con una marca de orden de bytes, que informa a una aplicación que recibe el archivo de que el archivo está ordenado por bytes.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Usar marcas de orden de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653089"
---
# <a name="using-byte-order-marks"></a><span data-ttu-id="1c865-103">Usar marcas de orden de bytes</span><span class="sxs-lookup"><span data-stu-id="1c865-103">Using Byte Order Marks</span></span>

<span data-ttu-id="1c865-104">Prefije siempre un archivo de texto sin formato Unicode con una marca de orden de bytes, que informa a una aplicación que recibe el archivo de que el archivo está ordenado por bytes.</span><span class="sxs-lookup"><span data-stu-id="1c865-104">Always prefix a Unicode plain text file with a byte order mark, which informs an application receiving the file that the file is byte-ordered.</span></span> <span data-ttu-id="1c865-105">En la tabla siguiente se enumeran las marcas de orden de bytes disponibles.</span><span class="sxs-lookup"><span data-stu-id="1c865-105">Available byte order marks are listed in the following table.</span></span> <span data-ttu-id="1c865-106">Dado que el texto sin formato Unicode es una secuencia de valores de código de 16 bits, es sensible al orden de bytes que se usa cuando se escribe el texto.</span><span class="sxs-lookup"><span data-stu-id="1c865-106">Because Unicode plain text is a sequence of 16-bit code values, it is sensitive to the byte ordering used when the text is written.</span></span>

> [!Note]  
> <span data-ttu-id="1c865-107">Una marca de orden de bytes no es un carácter de control que seleccione el orden de los bytes del texto.</span><span class="sxs-lookup"><span data-stu-id="1c865-107">A byte order mark is not a control character that selects the byte order of the text.</span></span>

 



| <span data-ttu-id="1c865-108">Marca de orden de bytes</span><span class="sxs-lookup"><span data-stu-id="1c865-108">Byte order mark</span></span> | <span data-ttu-id="1c865-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c865-109">Description</span></span>           |
|-----------------|-----------------------|
| <span data-ttu-id="1c865-110">EF BB BF</span><span class="sxs-lookup"><span data-stu-id="1c865-110">EF BB BF</span></span>        | <span data-ttu-id="1c865-111">UTF-8</span><span class="sxs-lookup"><span data-stu-id="1c865-111">UTF-8</span></span>                 |
| <span data-ttu-id="1c865-112">FF FE</span><span class="sxs-lookup"><span data-stu-id="1c865-112">FF FE</span></span>           | <span data-ttu-id="1c865-113">UTF-16, little endian</span><span class="sxs-lookup"><span data-stu-id="1c865-113">UTF-16, little endian</span></span> |
| <span data-ttu-id="1c865-114">FE FF</span><span class="sxs-lookup"><span data-stu-id="1c865-114">FE FF</span></span>           | <span data-ttu-id="1c865-115">UTF-16, big endian</span><span class="sxs-lookup"><span data-stu-id="1c865-115">UTF-16, big endian</span></span>    |
| <span data-ttu-id="1c865-116">FF FE 00 00</span><span class="sxs-lookup"><span data-stu-id="1c865-116">FF FE 00 00</span></span>     | <span data-ttu-id="1c865-117">UTF-32, little endian</span><span class="sxs-lookup"><span data-stu-id="1c865-117">UTF-32, little endian</span></span> |
| <span data-ttu-id="1c865-118">00 00 FE FF</span><span class="sxs-lookup"><span data-stu-id="1c865-118">00 00 FE FF</span></span>     | <span data-ttu-id="1c865-119">UTF-32, Big-Endian</span><span class="sxs-lookup"><span data-stu-id="1c865-119">UTF-32, big-endian</span></span>    |



 

> [!Note]  
> <span data-ttu-id="1c865-120">Microsoft usa UTF-16, little endian el orden de los bytes.</span><span class="sxs-lookup"><span data-stu-id="1c865-120">Microsoft uses UTF-16, little endian byte order.</span></span>

 

<span data-ttu-id="1c865-121">Idealmente, todo el texto Unicode sigue a un solo conjunto de reglas de ordenación de bytes.</span><span class="sxs-lookup"><span data-stu-id="1c865-121">Ideally, all Unicode text follows only one set of byte ordering rules.</span></span> <span data-ttu-id="1c865-122">Sin embargo, esto no es posible porque los microprocesadores difieren en la posición del byte menos significativo.</span><span class="sxs-lookup"><span data-stu-id="1c865-122">This is not possible, however, because microprocessors differ in the placement of the least significant byte.</span></span> <span data-ttu-id="1c865-123">Los procesadores Intel y MIPS colocan primero el byte menos significativo, mientras que los procesadores Motorola (y todos los archivos Unicode inversos en bytes) lo colocan en último lugar.</span><span class="sxs-lookup"><span data-stu-id="1c865-123">Intel and MIPS processors position the least significant byte first, whereas Motorola processors (and all byte-reversed Unicode files) position it last.</span></span> <span data-ttu-id="1c865-124">Con un solo conjunto de reglas de ordenación de bytes, los usuarios de un tipo de microprocesador deben cambiar el orden de los bytes cada vez que se lee o se escribe un archivo de texto sin formato, incluso si el archivo nunca se transfiere a otro sistema operativo basado en un microprocesador diferente.</span><span class="sxs-lookup"><span data-stu-id="1c865-124">With only a single set of byte ordering rules, users of one type of microprocessor are forced to swap the byte order every time a plain text file is read from or written to, even if the file is never transferred to another operating system based on a different microprocessor.</span></span>

<span data-ttu-id="1c865-125">El lugar preferido para especificar el orden de los bytes se encuentra en un encabezado de archivo, pero los archivos de texto no tienen encabezados.</span><span class="sxs-lookup"><span data-stu-id="1c865-125">The preferred place to specify byte order is in a file header, but text files do not have headers.</span></span> <span data-ttu-id="1c865-126">Por lo tanto, Unicode ha definido un carácter (U + FEFF) y un carácter (U + FFFE) como marcas de orden de bytes.</span><span class="sxs-lookup"><span data-stu-id="1c865-126">Therefore, Unicode has defined a character (U+FEFF) and a noncharacter (U+FFFE) as byte order marks.</span></span> <span data-ttu-id="1c865-127">Son imágenes de bytes reflejadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="1c865-127">They are mirror byte images of each other.</span></span>

<span data-ttu-id="1c865-128">Dado que la secuencia U + FEFF es más rara vez al principio de un archivo de texto no Unicode normal, puede actuar como marcador implícito o firma para identificar el archivo como un archivo Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c865-128">Since the sequence U+FEFF is exceedingly rare at the beginning of a regular non-Unicode text file, it can serve as an implicit marker or signature to identify the file as a Unicode file.</span></span> <span data-ttu-id="1c865-129">Las aplicaciones que leen archivos de texto Unicode y no Unicode deben usar la presencia de esta secuencia como un indicador de que es más probable que el archivo sea un archivo Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c865-129">Applications that read both Unicode and non-Unicode text files should use the presence of this sequence as an indicator that the file is most likely a Unicode file.</span></span> <span data-ttu-id="1c865-130">Compare esta técnica con el uso del marcador EOF de MS-DOS para terminar archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="1c865-130">Compare this technique to using the MS-DOS EOF marker to terminate text files.</span></span>

<span data-ttu-id="1c865-131">Cuando una aplicación encuentra U + FEFF al principio de un archivo de texto, normalmente procesa el archivo como un archivo Unicode, aunque puede realizar comprobaciones heurísticas adicionales para la comprobación.</span><span class="sxs-lookup"><span data-stu-id="1c865-131">When an application finds U+FEFF at the beginning of a text file, it typically processes the file as a Unicode file, although it can perform further heuristic checks for verification.</span></span> <span data-ttu-id="1c865-132">Este tipo de comprobación puede ser tan sencillo como realizar pruebas para averiguar si la variación en los bytes de orden inferior es mucho mayor que la variación en los bytes de orden superior.</span><span class="sxs-lookup"><span data-stu-id="1c865-132">Such a check can be as simple as testing to find out if the variation in the low-order bytes is much higher than the variation in the high-order bytes.</span></span> <span data-ttu-id="1c865-133">Por ejemplo, si el texto ASCII se convierte en texto Unicode, cada segundo byte es 0.</span><span class="sxs-lookup"><span data-stu-id="1c865-133">For example, if ASCII text is converted to Unicode text, every second byte is 0.</span></span> <span data-ttu-id="1c865-134">Además, la comprobación de los caracteres de avance de carro y retorno de carro (U + 000A y U + 000D) y para el tamaño de archivo par o impar puede proporcionar un indicador fuerte de la naturaleza del archivo.</span><span class="sxs-lookup"><span data-stu-id="1c865-134">Also, checking both for the linefeed and carriage return characters (U+000A and U+000D) and for even or odd file size can provide a strong indicator of the nature of the file.</span></span>

<span data-ttu-id="1c865-135">Cuando una aplicación encuentra U + FFFE al principio de un archivo de texto, lo interpreta para indicar que el archivo es un archivo Unicode invertido en bytes.</span><span class="sxs-lookup"><span data-stu-id="1c865-135">When an application finds U+FFFE at the beginning of a text file, it interprets it to mean that the file is a byte-reversed Unicode file.</span></span> <span data-ttu-id="1c865-136">La aplicación puede intercambiar el orden de los bytes o alertar al usuario de que se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="1c865-136">The application can either swap the order of the bytes or alert the user that an error has occurred.</span></span>

<span data-ttu-id="1c865-137">Puesto que el carácter de marca de orden de bytes Unicode no se encuentra en ninguna página de códigos, desaparece si los datos se convierten en ANSI.</span><span class="sxs-lookup"><span data-stu-id="1c865-137">Since the Unicode byte order mark character is not found in any code page, it disappears if data is converted to ANSI.</span></span> <span data-ttu-id="1c865-138">A diferencia de otros caracteres Unicode, no se sustituye por un carácter predeterminado cuando se convierte.</span><span class="sxs-lookup"><span data-stu-id="1c865-138">Unlike other Unicode characters, it is not replaced by a default character when it is converted.</span></span> <span data-ttu-id="1c865-139">Si se encuentra una marca de orden de bytes en medio de un archivo, no se interpreta como un carácter Unicode y no tiene ningún efecto en la salida de texto.</span><span class="sxs-lookup"><span data-stu-id="1c865-139">If a byte order mark is found in the middle of a file, it is not interpreted as a Unicode character and has no effect on text output.</span></span>

> [!Note]  
> <span data-ttu-id="1c865-140">El valor Unicode U + FFFF no es válido en archivos de texto sin formato y no puede pasarse entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1c865-140">The Unicode value U+FFFF is illegal in plain text files and cannot be passed between applications.</span></span> <span data-ttu-id="1c865-141">Está reservado para el uso privado de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1c865-141">It is reserved for the private use of an application.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1c865-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c865-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c865-143">Usar caracteres especiales en Unicode</span><span class="sxs-lookup"><span data-stu-id="1c865-143">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



