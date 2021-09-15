---
title: Funciones de palabras clave dinámicas de firewall
description: Las palabras clave dinámicas del firewall contienen las siguientes funciones.
keywords:
- Palabras clave dinámicas de firewall, funciones
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: d086c3aeb3caf7ff85a7fceeec17943c7112a7e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571709"
---
# <a name="firewall-dynamic-keywords-functions"></a>Funciones de palabras clave dinámicas de firewall

Las palabras clave dinámicas del firewall contienen las siguientes funciones.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | Solicita la entrega de notificaciones relacionadas con los cambios en determinados objetos de dirección de palabra clave dinámica[(FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)). |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | Cancela la entrega de notificaciones relacionadas con los cambios en determinados objetos de dirección de palabra clave dinámica[(FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)). |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | Tipo de puntero de función del punto de entrada del servicio al que se llama para agregar la dirección de palabra clave dinámica especificada. |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | Tipo de puntero de función del punto de entrada del servicio al que se llama para eliminar la dirección de palabra clave dinámica con el identificador especificado. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | Tipo de puntero de función del punto de entrada del servicio al que se llama para enumerar las direcciones de palabra clave dinámicas específicas por identificador. |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | Tipo de puntero de función del punto de entrada del servicio al que se llama para enumerar las direcciones de palabra clave dinámicas por tipo. Puede solicitar un subconjunto determinado de objetos en función de las marcas de enumeración pasadas. |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | Tipo de puntero de función del punto de entrada del servicio al que se llama para liberar los structs de datos de dirección de palabras clave dinámicas asignados por el servicio. |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | Tipo de puntero de función del punto de entrada del servicio al que se llama para actualizar la dirección de palabra clave dinámica con el identificador de entrada. |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de palabras clave dinámicas de firewall](firewall-dynamic-keywords-reference.md)
