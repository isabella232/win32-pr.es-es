---
title: Objeto agente de revocación de licencias
description: Objeto agente de revocación de licencias
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- SDK de Windows Media Format, objetos de agente de revocación de licencias
- Advanced Systems Format (ASF), objetos de agente de revocación de licencias
- ASF (formato de sistemas avanzados), objetos de agente de revocación de licencias
- objetos, objetos del agente de revocación de licencias
- revocación de licencias, objetos de agente de revocación de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420237"
---
# <a name="license-revocation-agent-object"></a>Objeto agente de revocación de licencias

El objeto agente de revocación de licencias administra el lado cliente de la revocación de licencia. La revocación de licencias es el proceso por el que un servidor de licencias puede quitar licencias del almacén de licencias en el equipo cliente. El proceso implica pasar varios mensajes entre la aplicación cliente y el servidor de licencias. Los métodos expuestos en este objeto procesan y generan esos mensajes.

El objeto agente de revocación de licencias se crea mediante la función [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , que establece un puntero a una interfaz [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) . **IUnknown** y **IWMLicenseRevocationAgent** son las únicas interfaces que admite este objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




