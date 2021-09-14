---
title: Objeto del agente de revocación de licencias
description: Objeto del agente de revocación de licencias
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows SDK de formato multimedia, objetos del agente de revocación de licencias
- Advanced Systems Format (ASF), objetos del agente de revocación de licencias
- ASF (formato de sistemas avanzados), objetos del agente de revocación de licencias
- objects,license revocation agent objects
- revocación de licencias, objetos del agente de revocación de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267087"
---
# <a name="license-revocation-agent-object"></a>Objeto del agente de revocación de licencias

El objeto del agente de revocación de licencias administra el lado cliente de la revocación de licencias. La revocación de licencias es el proceso por el que un servidor de licencias puede quitar licencias del almacén de licencias en el equipo cliente. El proceso implica pasar varios mensajes entre la aplicación cliente y el servidor de licencias. Los métodos expuestos en este proceso de objeto y generan esos mensajes.

La función [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) crea el objeto del agente de revocación de licencias, que establece un puntero a una [**interfaz IWMLicenseRevocationAgent.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) **IUnknown** e **IWMLicenseRevocationAgent** son las únicas interfaces compatibles con este objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




