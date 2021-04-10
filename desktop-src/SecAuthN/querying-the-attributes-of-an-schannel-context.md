---
description: Proporciona información específica de Schannel sobre un contexto de seguridad.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Consultar los atributos de un contexto Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153829"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Consultar los atributos de un contexto Schannel

La función [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) proporciona información específica de Schannel sobre un [*contexto de seguridad*](../secgloss/s-gly.md). La mayor parte de la información se especifica originalmente cuando el contexto se crea mediante la función de cliente [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) o Server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Se especifica cierta información al obtener un identificador de la credencial utilizada para crear el contexto. Para obtener más información, consulte [obtención de credenciales de Schannel](obtaining-schannel-credentials.md).

 

 
