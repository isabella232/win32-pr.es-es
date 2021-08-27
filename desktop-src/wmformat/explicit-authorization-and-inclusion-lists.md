---
title: Listas explícitas de autorización e inclusión
description: Listas explícitas de autorización e inclusión
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows SDK de formato multimedia, exportación de DRM
- Windows SDK de formato multimedia, exportar
- Windows SDK de formato multimedia, listas explícitas de inclusión y autorización
- Windows SDK de formato multimedia, listas de autorización
- Windows SDK de formato multimedia, listas de inclusión
- administración de derechos digitales (DRM),exportar
- DRM (administración de derechos digitales),exportar
- administración de derechos digitales (DRM), listas de inclusión y autorización explícitas
- DRM (administración de derechos digitales), listas de inclusión y autorización explícitas
- administración de derechos digitales (DRM),listas de autorización
- DRM (administración de derechos digitales),listas de autorización
- administración de derechos digitales (DRM),listas de inclusión
- DRM (administración de derechos digitales),listas de inclusión
- API extendidas de cliente DRM, listas explícitas de inclusión y autorización
- API extendidas de cliente, listas de inclusión y autorización explícitas
- API extendidas de cliente DRM, listas de autorización
- API extendidas de cliente, listas de autorización
- API extendidas de cliente DRM, listas de inclusión
- API extendidas de cliente, listas de inclusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee489d91002cacf7d8a0c89ffeef1752cd844aa089fabbe636e5e50fc185a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089735"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Listas explícitas de autorización e inclusión

Las licencias pueden contener una lista de inclusión para autorizar explícitamente la exportación de contenido protegido por Windows Drm multimedia a otros esquemas de protección de contenido (CPS). Según los términos del contrato de licencia que se firma con Microsoft para habilitar la exportación de DRM, solo puede exportar a una CPS válida que se identifique en la lista de inclusión de una licencia.

Una lista de inclusión es una matriz limitada de identificadores únicos globales (GUID) que cada uno representa un CPS autorizado específico al que se puede exportar el contenido. Los GUID enumerados en una lista de inclusión son independientes de los niveles de protección de salida (OPL) y de protección de contenido (CPL). Aplicar estas restricciones es responsabilidad de la aplicación.

> [!Note]  
> Al realizar Windows drm multimedia en contenido comprimido, se accede a la lista de inclusión a través del método [**IWMDRMLicense::GetInclusionList.**](iwmdrmlicense-getinclusionlist.md) Al realizar Windows drm multimedia en contenido sin comprimir, use el método [**IWMDRMReader3::GetInclusionList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist)

 

Para registrar un nuevo sistema de protección de contenido como Windows exportación permitida de DRM multimedia en las reglas de cumplimiento de exportación de DRM multimedia de Windows, póngase en contacto con wmla@microsoft.com .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Exportación de DRM**](drm-export.md)
</dt> </dl>

 

 




