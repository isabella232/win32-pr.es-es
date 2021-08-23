---
title: Solución de errores de firma de paquetes de aplicación
description: Un error de implementación de la aplicación puede deberse a un error al validar la firma digital del paquete de la aplicación. Obtenga información sobre cómo reconocer estos errores y qué hacer al respecto.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdec41d2d058a48153d6126fea534c1efaf16e16ccabef5d5e940daa73e839a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048953"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Solución de errores de firma de paquetes de aplicación

Un error de implementación de la aplicación puede deberse a un error al validar la firma digital del paquete de la aplicación. Obtenga información sobre cómo reconocer estos errores y qué hacer al respecto.

Al implementar una aplicación de Windows empaquetada, Windows siempre intenta validar la firma digital en el paquete de la aplicación. Errores durante la implementación de bloques de validación de firma del paquete. Pero el motivo por el que el paquete no se validó podría no ser obvio. En concreto, si firma los paquetes con certificados privados para pruebas locales, a menudo también debe administrar la confianza para esos certificados. Una configuración de confianza de certificado incorrecta puede provocar errores de validación de firmas.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Empaquetado, implementación y consulta de Windows aplicaciones](appx-portal.md)
-   [Comprobación de confianza de certificados](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Prerrequisitos

-   [Windows de eventos para](/windows/desktop/WES/windows-event-log) diagnosticar errores de instalación.
-   [Tareas certutiles para administrar certificados para la manipulación](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) del almacén de certificados durante la solución de problemas

## <a name="instructions"></a>Instructions

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Paso 1: Examen de los registros de eventos para obtener información de diagnóstico

Dependiendo de cómo haya intentado implementar la aplicación, es posible que no haya recibido un código de error significativo para el error de implementación. En este caso, normalmente puede obtener el código de error directamente de los registros de eventos.

**Para obtener el código de error de los registros de eventos**

1.  Ejecute **eventvwr.msc.**
2.  Vaya a **Visor de eventos registros de aplicaciones y servicios (locales)** de  >    >  **Microsoft**  >  **Windows**.
3.  El primer registro que se va a comprobar **es AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**.
4.  Los errores relacionados con la implementación se registran **en AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**.

    Para los errores de implementación, busque el evento de error 404 más reciente. Este evento de error proporciona el código de error y una descripción de por qué se produjo un error en la implementación. Si un evento de error 465 precedía al evento 404, se produjo un problema al abrir el paquete.

Si no se produjo el error 465, vea Solución de problemas generales de [empaquetado,](troubleshooting.md)implementación y consulta de Windows aplicaciones . De lo contrario, consulte esta tabla para ver los códigos de error comunes que pueden aparecer en la cadena de error para el evento de error 465:

| Código de error | Error                                 | Descripción                                                                                                          | Sugerencia                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | ERROR \_ AL INSTALAR OPEN PACKAGE \_ \_ \_ FAILED | No se pudo abrir el paquete de la aplicación.                                                                                 | Este error suele indicar un problema con el paquete. Debe compilar y firmar el paquete de nuevo. Para obtener más información, [consulte Uso de App Packager.](make-appx-package--makeappx-exe-.md) |
| 0x80080205 | APPX \_ E \_ INVALID \_ BLOCKMAP            | El paquete de la aplicación se ha alterado o tiene un mapa de bloques no válido.                                                  | El paquete está dañado. Debe compilar y firmar el paquete de nuevo. Para obtener más información, [consulte Uso de App Packager.](make-appx-package--makeappx-exe-.md)                                  |
| 0x800B0004 | TRUST \_ E \_ SUBJECT \_ NOT \_ TRUSTED       | El paquete de la aplicación se ha alterado.                                                                              | El contenido del paquete ya no coincide con su firma digital. Debe volver a firmar el paquete. Para obtener más información, [vea Cómo firmar un paquete de aplicación mediante SignTool.](how-to-sign-a-package-using-signtool.md)  |
| 0x800B0100 | TRUST \_ E \_ NOSIGNATURE                 | El paquete de la aplicación no tiene signo.                                                                                         | Solo se pueden implementar Windows paquetes de aplicaciones con firma. Para obtener información sobre cómo firmar un paquete de aplicación, [vea Cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md).                  |
| 0x800B0109 | RAÍZ \_ DE CERTIFICADO E QUE NO ES DE \_ \_ CONFIANZA              | La cadena de certificados que se usó para firmar el paquete de aplicación termina en un certificado raíz que no es de confianza.           | Continúe con el paso 2 para solucionar problemas de confianza de certificados.                                                                                                                                                  |
| 0x800B010A | \_ENCADENAMIENTO DE CERTIFICADOS E \_                     | No se pudo crear ninguna cadena de certificados en una entidad raíz de confianza del certificado que se usó para firmar el paquete de aplicación. | Continúe con el paso 2 para solucionar problemas de confianza de certificados.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Paso 2: Determinar la cadena de certificados usada para firmar el paquete de aplicación

Para averiguar los certificados en los que el equipo local debe confiar, puede examinar la cadena de certificados para la firma digital en el paquete de aplicación.

**Para determinar la cadena de certificados**

1.  En Explorador de archivos, haga clic con el botón derecho en el paquete de aplicación y seleccione **Propiedades.**
2.  En el **cuadro de** diálogo Propiedades, seleccione la **pestaña Firmas** digitales, que también muestra si se puede validar la firma.
3.  En la lista Firma, seleccione la firma y, a continuación, haga clic en **el botón** Detalles.
4.  En el cuadro **de diálogo Detalles de firma** digital, haga clic en el botón **Ver** certificado.
5.  En el cuadro **de diálogo** Certificado, seleccione la pestaña Ruta **de certificación.**

El certificado superior de la cadena es el certificado raíz y el certificado inferior es el certificado de firma. Si solo hay un certificado en la cadena, el certificado de firma también es su propio certificado raíz. Puede determinar el número de serie de cada certificado que use con [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)):

**Para determinar el número de serie de cada certificado**

1.  En el panel Ruta de certificación, seleccione el certificado y, a continuación, haga clic **en Ver certificado.**
2.  En el cuadro de diálogo Certificado, seleccione la **pestaña Detalles,** que muestra el número de serie y otras propiedades útiles del certificado.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Paso 3: Determinar los certificados de confianza de la máquina local

Para poder implementar un paquete de aplicación, no solo debe ser de confianza en el contexto del usuario, sino también en el contexto del equipo local. Como resultado, la firma digital puede parecer válida cuando se ve en la pestaña Firmas digitales del paso anterior, pero sigue sin validarse durante la implementación del paquete de aplicación.

**Para determinar si el equipo local confía específicamente en la cadena de certificados usada para firmar el paquete de aplicación**

1.  Ejecute este comando:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Ejecute este comando:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Si no especifica el número de serie del certificado, [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) enumera todos los certificados de confianza del equipo local para ese almacén.

El paquete puede no instalarse debido a errores de encadenamiento de certificados, incluso si el certificado de firma no es autofirmado y el certificado raíz está en el almacén raíz del equipo local. En este caso, podría haber un problema con la confianza para las autoridades de certificación intermedias. Para obtener más información sobre este problema, vea [Trabajar con certificados](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Comentarios

Si ha determinado que el paquete no se pudo implementar porque el certificado de firma no es de confianza, no instale el paquete a menos que sepa dónde se originó y confíe en él.

Si desea confiar manualmente en la aplicación para su instalación (por ejemplo, para instalar su propio paquete de aplicación firmado por pruebas), puede agregar manualmente el certificado a la confianza del certificado del equipo local desde el paquete de aplicación.

**Para agregar manualmente el certificado a la confianza de certificados del equipo local**

1.  En Explorador de archivos, haga clic con el botón derecho en el paquete de la aplicación y, en el menú contextual emergente, seleccione **Propiedades.**
2.  En el **cuadro de** diálogo Propiedades, seleccione la pestaña **Firmas digitales.**
3.  En la lista Firma, seleccione la firma y, a continuación, haga clic en **el botón** Detalles.
4.  En el cuadro **de diálogo Detalles de firma** digital, haga clic en el botón **Ver** certificado.
5.  En el cuadro **de diálogo** Certificado, haga clic en **Instalar certificado...** .
6.  En el Asistente para importación de certificados, seleccione **Equipo local y,** a continuación, haga clic **en Siguiente.** Tendrá que conceder privilegios de administrador para continuar.
7.  Seleccione **Colocar todos los certificados en el siguiente almacén y** vaya al almacén Personas **de** confianza.
8.  Haga **clic en Siguiente** y, a continuación, haga clic en Finalizar para completar el asistente. 

Después de esta adición manual, puede ver que el certificado ahora es de confianza en el **cuadro de diálogo** Certificado.

Puede quitar el certificado después de que ya no lo necesite.

**Para quitar el certificado**

1.  Ejecute **Cmd.exe** administrador.
2.  En el símbolo del sistema del administrador, ejecute este comando:

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Busque el número de serie del certificado que instaló. Este número es el *certID*.
4.  Ejecute este comando:

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

Se recomienda evitar agregar manualmente certificados raíz al equipo local entidades de certificación raíz de confianza [almacén de certificados](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store). Tener varias aplicaciones firmadas con certificados que se encadenar al mismo certificado raíz, como aplicaciones de línea de negocio, puede ser más eficaz que instalar certificados individuales en el almacén de personas de confianza. El almacén de personas de confianza contiene certificados que se consideran de confianza de forma predeterminada y, por tanto, no los comprueban las entidades superiores ni las cadenas o listas de confianza de certificados. Para obtener consideraciones sobre la adición de certificados al entidades de certificación raíz de confianza de certificados, vea [Procedimientos recomendados para](/previous-versions/windows/hardware/design/dn653556(v=vs.85))la firma de código.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Al agregar un certificado a almacenes [de certificados de equipo local,](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)afecta a la confianza de certificados de todos los usuarios del equipo. Se recomienda instalar los certificados de firma de código que desee para probar paquetes de aplicación en el almacén de certificados de personas de confianza. Quite rápidamente esos certificados cuando ya no sean necesarios, para evitar que se utilicen para poner en peligro la confianza del sistema. Si crea sus propios certificados de prueba para firmar paquetes de aplicación, también se recomienda restringir los privilegios asociados al certificado de prueba. Para obtener información sobre cómo crear certificados de prueba para firmar paquetes de aplicación, [consulte Creación de un certificado de firma de paquetes de aplicación.](how-to-create-a-package-signing-certificate.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Ejemplos**
</dt> <dt>

[Ejemplo de creación de paquete de aplicación](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceptos**
</dt> <dt>

[Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows](troubleshooting.md)
</dt> <dt>

[Tareas certutiles para administrar certificados](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 
