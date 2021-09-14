---
description: DDE de red proporciona funciones que permiten eliminar un recurso compartido, obtener o establecer información de recurso compartido, o enumerar recursos compartidos.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Administración de recursos compartidos de DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa89b890c9cf2b140f669b5e4dfa556cd11f978d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172318"
---
# <a name="managing-dde-shares"></a>Administración de recursos compartidos de DDE

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

DDE de red proporciona funciones que permiten eliminar un recurso compartido, obtener o establecer información de recurso compartido, o enumerar recursos compartidos.




| Tarea | Procedimiento | 
|------|-----------|
| Eliminación de un recurso compartido de DDE | Use la <a href="nddesharedel.md"><strong>función NDdeShareDel.</strong></a> | 
| Obtener información de recurso compartido de DDE | Use la <a href="nddesharegetinfo.md"><strong>función NDdeShareGetInfo.</strong></a> | 
| Establecer información de recurso compartido de DDE | Use la <a href="nddesharesetinfo.md"><strong>función NDdeShareSetInfo.</strong></a> | 
| Enumerar recursos compartidos de DDE | Use la <a href="nddeshareenum.md"><strong>función NDdeShareEnum.</strong></a> También puede enumerar los recursos compartidos de DDE de confianza mediante la <a href="nddetrustedshareenum.md"><strong>función NDdeTrustedShareEnum.</strong></a><br /> | 
| Enumerar usuarios conectados | Use la <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>función NetSessionEnum.</strong></a> | 
| Cambio del nombre del recurso compartido de DDE | Elimine el recurso compartido anterior y cree uno nuevo.<ol><li>Recupere la información del recurso compartido <a href="nddesharegetinfo.md"><strong>mediante NDdeShareGetInfo</strong></a>.</li><li>Quite el recurso compartido <a href="nddesharedel.md"><strong>mediante NDdeShareDel</strong></a>.</li><li>Cambie el <strong>miembro lpszShareName</strong> de la estructura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> devuelta <a href="nddesharegetinfo.md"><strong>por NDdeShareGetInfo</strong></a>.</li><li>Pase la estructura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modificada a <a href="nddeshareadd.md"><strong>NDdeShareAdd.</strong></a></li></ol> | 




 

 

