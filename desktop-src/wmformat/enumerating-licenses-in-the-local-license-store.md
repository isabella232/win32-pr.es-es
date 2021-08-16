---
title: Enumeración de licencias en el almacén de licencias local
description: Enumeración de licencias en el almacén de licencias local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows SDK de formato multimedia, enumeración de licencias
- Windows SDK de formato multimedia, licencias
- Windows SDK de formato multimedia, almacén de licencias local
- administración de derechos digitales (DRM), enumeración de licencias
- DRM (administración de derechos digitales), enumeración de licencias
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), almacén de licencias local
- DRM (administración de derechos digitales), almacén de licencias local
- API extendidas de cliente DRM, enumeración de licencias
- API extendidas de cliente, enumeración de licencias
- API extendidas de cliente DRM, licencias
- API extendidas de cliente, licencias
- API extendidas de cliente DRM, almacén de licencias local
- API extendidas de cliente, almacén de licencias local
- licenses,enumerating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27913a5a35ce9af1f5a4d6fa3cbae808bc2abe89afd5edb05aa927fe4c39227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848201"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Enumeración de licencias en el almacén de licencias local

La enumeración es un proceso de obtener información sobre las licencias en el almacén de licencias local, paso a paso por ellas una por una. Puede crear una enumeración de licencias llamando a [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).

La razón más común para enumerar a través de licencias en la tienda es encontrar una licencia determinada para el descifrado de algún contenido.

La [**interfaz IWMDRMLicense**](iwmdrmlicense.md) actúa como portal para los resultados individuales de la licencia y como enumerador. Cuando se crea la enumeración de licencias, la primera licencia de la lista se carga en la **interfaz IWMDRMLicense.** La mayoría de los métodos de **IWMDRMLicense** le permiten obtener información sobre la licencia o crear objetos para cifrar o descifrar contenido en función de la licencia. Sin embargo, hay dos métodos que controlan la enumeración: [**GetNext**](iwmdrmlicense-getnext.md) y [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md). **GetNext** carga la siguiente licencia de la lista en la interfaz . **ResetEnumeration** devuelve la enumeración al estado en el que estaba cuando se creó por primera vez. Cuando se restablece la enumeración, la primera licencia de la lista se vuelve a cargar en la **interfaz IWMDRMLicense.**

Cuando haya alcanzado la última licencia de la lista, la siguiente llamada a **GetNext** devuelve ERROR \_ NO MORE \_ \_ ITEMS.

Si la aplicación realiza una acción con el contenido que está cubierto por DRM, debe comprobar las licencias del almacén de licencias local para obtener los derechos y otros factores de limitación, como los niveles de protección de salida (OLO).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de licencias en el almacén de licencias local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




