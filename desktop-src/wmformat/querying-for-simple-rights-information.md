---
title: Consulta de información de derechos simples
description: Consulta de información de derechos simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- Windows SDK de formato multimedia, consulta de derechos simples
- Windows SDK de formato multimedia, consultas de derechos simples
- administración de derechos digitales (DRM), consulta de derechos simples
- DRM (administración de derechos digitales), consulta de derechos simples
- digital rights management (DRM), consultas de derechos simples
- DRM (administración de derechos digitales), consultas de derechos simples
- API extendidas de cliente DRM, consulta de derechos simples
- API extendidas de cliente, consulta de derechos simples
- API extendidas de cliente DRM, consultas de derechos simples
- API extendidas de cliente, consultas de derechos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0686616bbc700c51a005c3e1e63eed889c42965aaebbba232fcf90b9cce26987
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027373"
---
# <a name="querying-for-simple-rights-information"></a>Consulta de información de derechos simples

Las API extendidas Windows de cliente DRM multimedia permiten obtener rápidamente información sencilla sobre si se puede acceder al contenido protegido para diversas acciones.

El [**método IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) se puede usar para determinar rápidamente si una licencia permite una acción en el almacén de licencias local. **QueryActionAllowed** se ha optimizado para ser mucho más rápido que las consultas de información similar mediante los objetos del SDK Windows Media Format. Sin embargo, este tipo de consulta agrega las licencias en el almacén de licencias local y solo se debe usar para características sencillas, como puede ser necesario para los elementos de la interfaz de usuario, por ejemplo, mostrar un indicador de permiso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de licencias en el almacén de licencias local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




