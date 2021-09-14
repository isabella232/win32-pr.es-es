---
description: Proporciona información específica de Schannel sobre un contexto de seguridad.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Consulta de los atributos de un contexto de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160973"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Consulta de los atributos de un contexto de Schannel

La [**función QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) proporciona información específica de Schannel sobre un contexto [*de seguridad*](../secgloss/s-gly.md). La mayor parte de la información se especifica originalmente cuando el contexto se crea mediante la función [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) o [**el servidor AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) del cliente. Se especifica cierta información al obtener un identificador para la credencial utilizada para crear el contexto. Para obtener más información, vea [Obtención de credenciales de Schannel.](obtaining-schannel-credentials.md)

 

 
