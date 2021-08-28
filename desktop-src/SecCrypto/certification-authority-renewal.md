---
description: Servicios de certificados admite la renovación de una entidad de certificación (CA).
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Renovación de la entidad de certificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f486e877e2ce1645cddf0099599e120776194dfd71e4e8b131d936c85e1f45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993115"
---
# <a name="certification-authority-renewal"></a>Renovación de la entidad de certificación

[*Servicios de certificados*](../secgloss/c-gly.md) admite la renovación de [*una entidad de certificación*](../secgloss/c-gly.md) (CA). La renovación es la emisión de un nuevo certificado para que la CA amplíe la vida de la entidad de certificación más allá de la fecha de finalización de su certificado original. Puede renovar una CA como una tarea en el complemento MMC de la entidad de certificación o mediante la herramienta Certutil.exe (con el **comando -renewCert).**

Cada renovación da como resultado un nuevo certificado de entidad de certificación; sin embargo, el administrador puede generar un nuevo par de claves pública y privada o reutilizar el par de claves pública y privada existente para el certificado de entidad de certificación. Por coherencia e integridad, los certificados de entidad de certificación y las listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) emitidos por la CA antes de su renovación estarán disponibles una vez que se haya renovado la CA. Para que estén disponibles, Servicios de certificados mantiene un índice de certificados de entidad de certificación, CRL y claves.

Los índices y los nombres de sufijo de certificados de entidad de certificación y CRL durante varias operaciones de renovación de ca son los siguientes.



| Operación                | Índice de certificado de entidad de certificación | Sufijo de nombre de archivo de certificado de entidad de certificación | CRL y índice de clave | CRL y sufijo de nombre de contenedor de claves |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Instalación de ca original | 0                    | ""                              | 0                 | ""                                |
| Renovación con nueva clave     | 1                    | "(1)"                           | 1                 | "(1)"                             |
| Clave de reuso de renovación      | 2                    | "(2)"                           | 1                 | "(1)"                             |
| Clave de reuso de renovación      | 3                    | "(3)"                           | 1                 | "(1)"                             |
| Renovación con nueva clave     | 4                    | "(4)"                           | 4                 | "(4)"                             |
| Clave de reuso de renovación      | 5                    | "(5)"                           | 4                 | "(4)"                             |
| Renovación con nueva clave     | 6                    | "(6)"                           | 6                 | "(6)"                             |
| Clave de reuso de renovación      | 7                    | "(7)"                           | 6                 | "(6)"                             |



 

Cuando se instala una entidad de certificación, el índice de certificado es cero y el sufijo del certificado es "" (una cadena vacía). Cada vez que se renueva el certificado (independientemente de si se reutilizan o no las claves), el índice del certificado se incrementa en uno y el sufijo de nombre de archivo de certificado se convierte en una cadena con el formato "(*n*)", donde *n* representa el número de veces que se ha renovado el certificado de entidad de certificación. Después de la primera renovación, el índice de certificado es 1 y el sufijo del nombre del archivo de certificado es "(1)". Después de la segunda renovación, el índice de certificado es 2 y el sufijo del nombre del archivo de certificado es "(2)", y así sucesivamente.

Aunque el sufijo y el índice de certificado de entidad de certificación se incrementan en uno cada vez que se renueva la entidad de certificación, los índices de clave y CRL y los sufijos de nombre de archivo se establecen en el índice de certificado de entidad de certificación solo si el proceso de renovación incluye un nuevo par de claves pública y privada. Si no es así, los valores de estos índices y sufijos siguen siendo los mismos que para el último índice. Durante la renovación, un administrador especifica si se genera un nuevo par de claves o se usa el par de claves existente. (En el complemento MMC de la entidad de certificación, una opción de la interfaz de usuario especifica un par de claves nuevo o existente; en la herramienta Certutil.exe, el comando **certutil -renewCert** renueva la CA con un nuevo par de claves, mientras que el comando **certutil -renewCert ReuseKeys** renueva la CA con el par de claves existente).

El índice CRL está asociado directamente al índice de clave, que se establece en el índice de certificado de entidad de certificación solo cuando se usa un nuevo par de claves para la renovación. Después de la primera renovación (que usó un nuevo par de claves), el índice de la CRL y la clave se establece en 1, y el sufijo de nombre de contenedor de claves y CRL es "(1)". Sin embargo, después de la segunda renovación, el índice de la CRL y la clave permanecen en 1, y el sufijo de nombre del contenedor de claves y la CRL también permanecen "(1)"; Esto se debe a que la segunda renovación usó el par de claves existente y solo se emite una CRL para cada par de claves de ca.

Puede recuperar los certificados de entidad de certificación indexados y las CRL llamando al método **GetCertificateProperty** (en las interfaces [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) e [**ICertServerPolicy).**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Al recuperar determinadas propiedades relacionadas con el certificado de entidad de certificación o CRL, puede anexar el índice de base cero del certificado de entidad de certificación a los nombres de propiedad. Por ejemplo, para recuperar el índice CRL que corresponde al tercer certificado de la entidad de certificación, pase la propiedad "CRLIndex.2" a [**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); para la tabla, el valor de propiedad "CRLIndex.2" recuperado sería 1. Se puede usar una propiedad denominada "CertCount" para determinar el número de veces que se ha emitido un certificado de CA a la CA.

Los certificados de entidad de certificación y las CRL contienen una extensión que proporciona información sobre el certificado y el índice de clave. La extensión se define en Wincrypt.h como szOID CERTSRV CA VERSION con un valor \_ \_ de \_ "1.3.6.1.4.1.311.21.1". Los datos de extensión son un valor **DWORD** (codificado como INTEGER X509 en la extensión); los 16 bits inferiores son el índice de certificado y los 16 bits altos son el índice de \_ clave.

La instalación inicial de una entidad de certificación genera un índice de certificado de cero y un índice de clave de cero. La renovación de un certificado de entidad de certificación hará que se incremente el índice de certificado. Si la clave se reutiliza en la renovación, el índice de clave será el mismo que el índice de clave anterior. Si la clave no se reutiliza, el índice de clave coincidirá con el nuevo índice de certificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
