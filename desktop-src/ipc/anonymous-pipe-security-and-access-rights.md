---
description: Puede especificar un descriptor de seguridad para una canalización anónima cuando llame a la función CreatePipe. El descriptor de seguridad controla el acceso a los extremos de lectura y escritura de la canalización.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Seguridad de canalización anónima y derechos de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688521"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Seguridad de canalización anónima y derechos de acceso

La seguridad de Windows le permite controlar el acceso a las canalizaciones anónimas. Para obtener más información sobre la seguridad, vea [modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).

Puede especificar un [descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors) para una canalización cuando llame a la función [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) . El descriptor de seguridad controla el acceso a los extremos de lectura y escritura de la canalización. Si especifica **null**, la canalización obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para una canalización proceden del token principal o de suplantación del creador.

Para recuperar el descriptor de seguridad de una canalización, llame a la función [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Para cambiar el descriptor de seguridad de una canalización, llame a la función [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

La función [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) devuelve dos identificadores para la canalización anónima: un controlador de lectura con acceso genérico de \_ lectura y sincronización, y un identificador de escritura con \_ acceso de escritura y sincronización genéricos. \_Los accesos genéricos de lectura y \_ escritura usan la misma asignación de derechos de acceso que para las canalizaciones con nombre.

El \_ acceso de lectura genérico para una canalización anónima combina los derechos para leer los datos de la canalización, leer los atributos de la canalización, leer atributos extendidos y leer la DACL de la canalización.

\_El acceso de escritura genérico para una canalización anónima combina los derechos para escribir datos en la canalización, anexar datos a él, escribir atributos de canalización, escribir atributos extendidos y leer la DACL de la canalización.

 

 
