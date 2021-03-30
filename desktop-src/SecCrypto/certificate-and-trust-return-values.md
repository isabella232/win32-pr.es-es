---
description: Enumera los valores devueltos de certificado y confianza de certificado. Estos valores se encuentran en el archivo de encabezado Winerror. h.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Valores devueltos de certificado y confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e17f170c7c3aa1ac0839323b9a52767a101dd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809457"
---
# <a name="certificate-and-trust-return-values"></a>Valores devueltos de certificado y confianza

En la tabla siguiente se enumeran los valores devueltos de certificado y confianza de certificado. Estos valores se encuentran en el archivo de encabezado Winerror. h.



| Nombre                            | Descripción                                                                                                                    | Value      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| CERTIFICADO \_ E \_ crítico               | Un certificado contiene una extensión desconocida marcada como "crítica".                                                         | 0x800B0105 |
| nombre de certificado \_ E \_ no válido \_          | El certificado tiene un nombre que no es válido. El nombre no está incluido en la lista permitida o está explícitamente excluido. | 0x800B0114 |
| CERTIFICADO \_ E \_ Directiva no válida \_        | El certificado tiene una directiva que no es válida.                                                                                | 0x800B0113 |
| CERT \_ E \_ ISSUERCHAINING         | En realidad, un elemento primario de un certificado determinado no ha emitido ese certificado secundario.                                                  | 0x800B0107 |
| el certificado E tiene un \_ \_ formato incorrecto              | Falta un certificado o tiene un valor vacío para un campo importante, como un nombre de asunto o de emisor.                       | 0x800B0108 |
| CERT \_ E \_ PATHLENCONST           | Se ha infringido una restricción de longitud de ruta de acceso en la cadena de la certificación.                                                         | 0x800B0104 |
| CERT \_ E \_ UNTRUSTEDCA            | Una cadena de certificación se procesó correctamente, pero el proveedor de directivas no confía en uno de los certificados de entidad de certificación.               | 0x800B0112 |
| CIFRAr \_ E \_ no \_ comprobar la revocación \_ | La función de revocación no pudo comprobar la revocación del certificado.                                                    | 0x80092012 |
| CONFIANZA \_ E \_ \_ Resumen incorrecto           | No se ha comprobado la firma digital del objeto.                                                                            | 0x80096010 |
| CONFIAR en \_ restricciones de E \_ Basic \_    | No se ha observado la extensión de la restricción básica de un certificado.                                                         | 0x80096019 |
| CONFIANZA \_ E \_ firma de certificado \_       | No se puede comprobar la firma del certificado.                                                                           | 0x80096004 |
| CONFIAR en el firmante de \_ E \_ \_       | Una de las firmas de contador no era válida.                                                                                   | 0x80096003 |
| CONFIAR \_ E \_ \_ desconfiar explícitos    | El usuario marcó explícitamente el certificado como no de confianza.                                                                | 0x800B0111 |
| CONFIAR \_ en \_ criterios financieros E \_   | El certificado no cumple ni contiene las extensiones financieras de Authenticode.                                                | 0x8009601E |
| TRUST \_ E \_ sin \_ firmante \_ CERT      | El certificado para el firmante del mensaje no es válido o no se encuentra.                                                       | 0x80096002 |
| ERROR de sistema de confianza \_ E \_ \_         | Se ha producido un error del nivel de sistema al comprobar la confianza.                                                                           | 0x80096001 |
| marca de tiempo de confianza \_ E \_ \_           | La firma o el certificado de la marca de tiempo no se ha podido comprobar o es incorrecta.                                                 | 0x80096005 |



 

 

 



