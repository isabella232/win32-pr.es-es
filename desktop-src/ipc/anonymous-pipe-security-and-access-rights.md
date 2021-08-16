---
description: Puede especificar un descriptor de seguridad para una canalización anónima al llamar a la función CreatePipe. El descriptor de seguridad controla el acceso a los extremos de lectura y escritura de la canalización.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Seguridad de canalización anónima y derechos de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b54869584a70bfbe886740e979c44864d852de0df23e311eb4aad89c321662c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756362"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Seguridad de canalización anónima y derechos de acceso

Windows seguridad le permite controlar el acceso a las canalizaciones anónimas. Para obtener más información sobre la seguridad, vea [Modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).

Puede especificar un [descriptor de seguridad para](/windows/desktop/SecAuthZ/security-descriptors) una canalización al llamar a la función [**CreatePipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) El descriptor de seguridad controla el acceso a los extremos de lectura y escritura de la canalización. Si especifica **NULL,** la canalización obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para una canalización proceden del token principal o de suplantación del creador.

Para recuperar el descriptor de seguridad de una canalización, llame a la [**función GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Para cambiar el descriptor de seguridad de una canalización, llame a la [**función SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

La [**función CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) devuelve dos identificadores a la canalización anónima: un identificador de lectura con acceso GENERIC READ y SYNCHRONIZE; y un identificador de escritura con \_ acceso GENERIC WRITE y \_ SYNCHRONIZE. El \_ acceso DE LECTURA GENÉRICA y ESCRITURA GENÉRICA usa la misma \_ asignación de derechos de acceso que para las canalizaciones con nombre.

El acceso DE LECTURA GENÉRICO para una canalización anónima combina los derechos para leer datos de la canalización, leer atributos de canalización, leer atributos extendidos y leer la DACL de la \_ canalización.

El acceso DE ESCRITURA GENÉRICO para una canalización anónima combina los derechos para escribir datos en la canalización, anexar datos a ella, escribir atributos de canalización, escribir atributos extendidos y leer la DACL de la \_ canalización.

 

 
