---
title: Enumerar licencias en el almacén de licencias local
description: Enumerar licencias en el almacén de licencias local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK, enumerar licencias
- SDK de Windows Media Format, licencias
- SDK de Windows Media Format, almacén de licencias local
- Administración de derechos digitales (DRM), enumerar licencias
- DRM (administración de derechos digitales), enumerar licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), almacén de licencias local
- DRM (administración de derechos digitales), almacén de licencias local
- API extendidas del cliente DRM, enumerar licencias
- API extendidas del cliente, enumerar licencias
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, almacén de licencias local
- API extendidas de cliente, almacén de licencias local
- licencias, enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418520"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Enumerar licencias en el almacén de licencias local

La enumeración es un proceso que consiste en obtener información acerca de las licencias en el almacén de licencias local, ya que se recorren una por una. Puede crear una enumeración de licencias mediante una llamada a [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).

La razón más común para enumerar licencias en el almacén es encontrar una licencia concreta para el descifrado de algún contenido.

La interfaz [**IWMDRMLicense**](iwmdrmlicense.md) sirve como portal para los resultados de licencia individuales y como enumerador. Cuando se crea la enumeración de licencias, la primera licencia de la lista se carga en la interfaz **IWMDRMLicense** . La mayoría de los métodos de **IWMDRMLicense** permiten obtener información sobre la licencia o crear objetos para cifrar o descifrar el contenido en función de la licencia. Sin embargo, hay dos métodos que controlan la enumeración: [**Getnext**](iwmdrmlicense-getnext.md) y [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md). **Getnext** carga la siguiente licencia de la lista en la interfaz. **ResetEnumeration** devuelve la enumeración al estado en que se encontraba cuando se creó por primera vez. Cuando se restablece la enumeración, la primera licencia de la lista se vuelve a cargar en la interfaz **IWMDRMLicense** .

Cuando se ha alcanzado la última licencia de la lista, la siguiente llamada a **Getnext** devuelve el error \_ no hay \_ más \_ elementos.

Si la aplicación realiza una acción con el contenido que está incluido en DRM, debe comprobar las licencias en el almacén de licencias local para los derechos y otros factores de limitación, como los niveles de protección de salida (OPLs).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de licencias en el almacén de licencias local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




