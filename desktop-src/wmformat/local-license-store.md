---
title: Almacén de licencias local
description: Almacén de licencias local
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- Windows SDK de formato multimedia, licencias DRM
- Windows SDK de formato multimedia, licencias para DRM
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- licenses,DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267063"
---
# <a name="local-license-store"></a>Almacén de licencias local

Cuando se entrega una licencia DRM al equipo cliente, se coloca en el almacén de licencias local. Se trata de un archivo protegido en el disco duro que contiene todas las licencias emitidas al usuario junto con otra información de DRM.

Puede manipular los datos en el almacén de licencias local de varias maneras limitadas mediante el uso de las API extendidas de cliente DRM de Windows media.

Además del almacén de licencias local, algunos objetos usan un almacén de licencias temporal. Una licencia de un almacén temporal solo existe durante un breve período de tiempo. Sin embargo, algunas licencias que comienzan en un almacén temporal se pueden guardar en el almacén de licencias local normal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](drmconcepts.md)
</dt> </dl>

 

 




