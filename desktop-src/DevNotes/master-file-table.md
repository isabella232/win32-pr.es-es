---
description: La tabla de archivos maestros (MFT) almacena la información necesaria para recuperar archivos de una partición NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabla de archivos maestros (notas del desarrollador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998091"
---
# <a name="master-file-table"></a>Tabla de archivos maestros

\[Este documento solo se aplica a la versión 3 de los volúmenes NTFS.\]

La tabla de archivos maestros (MFT) almacena la información necesaria para recuperar archivos de una partición NTFS.

Un archivo puede tener uno o más registros MFT y puede contener uno o más atributos. En NTFS, una referencia de archivo es la referencia de segmento MFT del registro de archivo base. Para obtener más información, [**consulte \_ \_ referencia de segmentos de MFT**](mft-segment-reference.md).

La MFT contiene segmentos de registro de archivos; los primeros 16 están reservados para archivos especiales, como los siguientes:

-   0: MFT ($Mft)
-   5: directorio raíz ( \\ )
-   6: archivo de asignación de clúster de volumen ($Bitmap)
-   8: archivo de clúster incorrecto ($BadClus)

Cada segmento de registro de archivo comienza con un encabezado de segmento de registro de archivo. Para obtener más información, [**consulte \_ \_ \_ encabezado de segmento de registro de archivo**](file-record-segment-header.md). Cada segmento de registro de archivo va seguido de uno o varios atributos. Cada atributo comienza con un encabezado de registro de atributo. Para obtener más información, consulte [**Attribute \_ Record \_ Header**](attribute-record-header.md). El registro del atributo incluye el tipo de atributo (como $DATA o $BITMAP), un nombre opcional y el valor del atributo. El flujo de datos de usuario es un atributo, al igual que todos los flujos. La lista de atributos finaliza con 0xFFFFFFFF ($END).

A continuación se muestran algunos atributos de ejemplo.

-   El archivo de $Mft contiene un atributo de $DATA sin nombre que es la secuencia de segmentos de registro de MFT, en orden.
-   El archivo de $Mft contiene un atributo de $BITMAP sin nombre que indica qué registros de MFT están en uso.
-   El archivo de $Bitmap contiene un atributo de $DATA sin nombre que indica qué clústeres están en uso.
-   El archivo de $BadClus contiene un atributo de $DATA denominado $BAD que contiene una entrada que corresponde a cada clúster incorrecto.

Cuando no hay más espacio para almacenar los atributos en el segmento de registro de archivo, los segmentos de registro de archivos adicionales se asignan y se insertan en el primer segmento de registro de archivo (o base) en un atributo denominado lista de atributos. La lista de atributos indica dónde se puede encontrar cada atributo asociado al archivo. Esto incluye todos los atributos del registro de archivo base, excepto la propia lista de atributos. Para obtener más información, [**consulte \_ \_ entrada**](attribute-list-entry.md)de la lista de atributos.

Entre las estructuras relacionadas con MFT se incluyen las siguientes:

-   [**\_entrada de lista de atributos \_**](attribute-list-entry.md)
-   [**\_encabezado de registro de atributo \_**](attribute-record-header.md)
-   [**nombre de archivo \_**](file-name.md)
-   [**\_encabezado de \_ segmento de registro de archivo \_**](file-record-segment-header.md)
-   [**\_referencia de segmento de MFT \_**](mft-segment-reference.md)
-   [**encabezado de varios \_ sectores \_**](multi-sector-header.md)
-   [**\_información estándar**](standard-information.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia técnica de NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
