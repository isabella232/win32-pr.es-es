---
description: Servicios de Certificate Server admite la renovación de una entidad de certificación (CA).
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Renovación de la entidad de certificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de57cd16ae6fc4c90bfeea411a06efcb14d028b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001424"
---
# <a name="certification-authority-renewal"></a>Renovación de la entidad de certificación

[*Servicios de Certificate Server*](../secgloss/c-gly.md) admite la renovación de una [*entidad de certificación*](../secgloss/c-gly.md) (CA). La renovación es la emisión de un nuevo certificado para que la entidad de certificación extienda la vida de la entidad de certificación más allá de la fecha de finalización de su certificado original. Puede renovar una entidad de certificación como una tarea dentro del complemento MMC de la entidad de certificación o mediante la herramienta de Certutil.exe (con el comando **-renewCert** ).

Cada renovación da como resultado un nuevo certificado de CA. sin embargo, el administrador puede generar un nuevo par de claves pública y privada, o volver a usar el par de claves pública y privada existente para el certificado de CA. Para mantener la coherencia y la integridad, los certificados de CA y [*las listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) emitidos por la CA antes de su renovación estarán disponibles después de renovar la CA. Para que estén disponibles, servicios de Certificate Server mantiene un índice de certificados de entidad de certificación, CRL y claves.

Los índices y los nombres de sufijo de los certificados y las CRL de CA durante varias operaciones de renovación de CA son los siguientes.



| Operación                | Índice de certificado de CA | Sufijo de nombre de archivo de certificado de CA | CRL e índice de clave | Sufijo de nombre de contenedor de claves y CRL |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Instalación de la CA original | 0                    | ""                              | 0                 | ""                                |
| Renovación con clave nueva     | 1                    | "(1)"                           | 1                 | "(1)"                             |
| Renovación de la clave de reutilización      | 2                    | "(2)"                           | 1                 | "(1)"                             |
| Renovación de la clave de reutilización      | 3                    | "(3)"                           | 1                 | "(1)"                             |
| Renovación con clave nueva     | 4                    | "(4)"                           | 4                 | "(4)"                             |
| Renovación de la clave de reutilización      | 5                    | "(5)"                           | 4                 | "(4)"                             |
| Renovación con clave nueva     | 6                    | "(6)"                           | 6                 | "(6)"                             |
| Renovación de la clave de reutilización      | 7                    | "(7)"                           | 6                 | "(6)"                             |



 

Cuando se instala una CA, el índice de certificado es cero y el sufijo del certificado es "" (una cadena vacía). Cada vez que se renueva el certificado (tanto si se reutilizan las claves como si no), el índice del certificado se incrementa en uno, y el sufijo del nombre del archivo del certificado se convierte en una cadena con el formato "(*n*)", donde *n* representa el número de veces que se ha renovado el certificado de la entidad de certificación. Después de la primera renovación, el índice del certificado es 1 y el sufijo del nombre del archivo del certificado es "(1)". Después de la segunda renovación, el índice del certificado es 2 y el sufijo del nombre del archivo del certificado es "(2)", y así sucesivamente.

Aunque el índice y el sufijo del certificado de entidad de certificación se incrementan en uno cada vez que se renueva la CA, los índices de clave y de CRL y los sufijos de nombre de archivo se establecen en el índice de certificado de CA solo si el proceso de renovación incluye un nuevo par de claves pública y privada. Si no es así, los valores de estos índices y sufijos siguen siendo los mismos que para el último índice. Durante la renovación, un administrador especifica si se genera un nuevo par de claves o si se usa el par de claves existente. (En el complemento MMC de la entidad de certificación, una opción de la interfaz de usuario especifica un par de claves nuevo o existente; en la herramienta Certutil.exe, el comando **certutil-renewCert** renueva la CA con un nuevo par de claves, mientras que el comando **certutil-renewCert ReuseKeys** renueva la CA con el par de claves existente).

El índice de CRL está directamente vinculado al índice de clave, que se establece en el índice de certificado de CA solo cuando se usa un nuevo par de claves para la renovación. Después de la primera renovación (que usaba un nuevo par de claves), el índice de la CRL y la clave se establece en 1, y el sufijo de la CRL y el nombre del contenedor de claves es "(1)". Sin embargo, después de la segunda renovación, el índice de la CRL y la clave sigue siendo 1, y la CRL y el sufijo del nombre del contenedor de claves también permanecen "(1)"; Esto se debe a que la segunda renovación usó el par de claves existente y solo se emite una CRL para cada par de claves de CA.

Puede recuperar los certificados y las CRL de CA indexados llamando al método **GetCertificateProperty** (en las interfaces [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) y [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) ). Al recuperar ciertas propiedades relacionadas con el certificado o la CRL de la entidad de certificación, puede anexar el índice basado en cero del certificado de la entidad de certificación a los nombres de propiedad. Por ejemplo, para recuperar el índice de CRL que corresponde al tercer certificado de la entidad de certificación, pase la propiedad "CRLIndex. 2" a [**ICertServerPolicy:: GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); en el caso de la tabla, el valor de la propiedad "CRLIndex. 2" recuperada sería 1. Se puede usar una propiedad denominada "CertCount" para determinar el número de veces que se ha emitido un certificado de CA a la entidad de certificación.

Los certificados y las CRL de CA contienen una extensión que proporciona información sobre el certificado y el índice de claves. La extensión se define en Wincrypt. h como \_ \_ versión de la entidad de certificación szOID CERTSRV \_ con un valor de "1.3.6.1.4.1.311.21.1". Los datos de la extensión son un valor **DWORD** (codificado como \_ entero X509 en la extensión); los 16 bits inferiores son el índice de certificado y los 16 bits superiores son el índice de clave.

La instalación inicial de una CA genera un índice de certificado de cero y un índice de clave de cero. La renovación de un certificado de entidad de certificación hará que se incremente el índice de certificado. Si la clave se reutiliza en la renovación, el índice de clave será el mismo que el índice de clave anterior. Si no se reutiliza la clave, el índice de clave coincidirá con el nuevo índice de certificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
