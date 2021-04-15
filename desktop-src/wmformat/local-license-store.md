---
title: Almacén de licencias local
description: Almacén de licencias local
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419132"
---
# <a name="local-license-store"></a>Almacén de licencias local

Cuando se entrega una licencia DRM en el equipo cliente, se coloca en el almacén de licencias local. Se trata de un archivo protegido en el disco duro que contiene todas las licencias emitidas al usuario junto con otra información de DRM.

Puede manipular los datos en el almacén de licencias local de algunas maneras limitadas mediante el uso de las API extendidas del cliente DRM de Windows Media.

Además del almacén de licencias local, algunos objetos hacen uso de un almacén de licencias temporal. Una licencia de un almacén temporal solo existe durante un breve período de tiempo. Sin embargo, algunas licencias que comienzan en un almacén temporal se pueden guardar en el almacén de licencias local normal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](drmconcepts.md)
</dt> </dl>

 

 




