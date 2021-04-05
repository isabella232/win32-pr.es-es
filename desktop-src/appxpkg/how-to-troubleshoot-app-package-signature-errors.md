---
title: Cómo solucionar errores de firma de paquete de aplicaciones
description: Un error de implementación de la aplicación puede deberse a un error al validar la firma digital del paquete de la aplicación. Obtenga información acerca de cómo reconocer estos errores y qué hacer con ellos.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0afe77ebfd478be5c652604ea575fc90b5d3ef
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104420525"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Cómo solucionar errores de firma de paquete de aplicaciones

Un error de implementación de la aplicación puede deberse a un error al validar la firma digital del paquete de la aplicación. Obtenga información acerca de cómo reconocer estos errores y qué hacer con ellos.

Cuando se implementa una aplicación de Windows empaquetada, Windows siempre intenta validar la firma digital en el paquete de la aplicación. Errores durante la validación de la firma bloquean la implementación del paquete. Pero por qué el paquete no se validó podría no ser obvio. En concreto, si firma los paquetes con certificados privados para las pruebas locales, a menudo debe administrar la confianza para esos certificados también. Una configuración de confianza de certificados incorrecta puede provocar errores de validación de la firma.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Empaquetado, implementación y consulta de aplicaciones de Windows](appx-portal.md)
-   [Comprobación de certificados de confianza](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Requisitos previos

-   [Registro de eventos de Windows](/windows/desktop/WES/windows-event-log) para diagnosticar errores de instalación.
-   [Tareas certutil para administrar certificados](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) para la manipulación del almacén de certificados durante la solución de problemas

## <a name="instructions"></a>Instrucciones

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Paso 1: examinar los registros de eventos para obtener información de diagnóstico

En función de cómo intente implementar la aplicación, es posible que no haya recibido un código de error significativo para el error de implementación. En este caso, normalmente puede obtener el código de error directamente de los registros de eventos.

**Para obtener el código de error de los registros de eventos**

1.  Ejecute **eventvwr. msc**.
2.  Vaya a **visor de eventos (local)**  >  **registros de aplicaciones y servicios**  >  **Microsoft**  >  **Windows**.
3.  El primer registro que se va a comprobar es **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**.
4.  Los errores relacionados con la implementación se registran en **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**.

    En el caso de los errores de implementación, busque el evento de error 404 más reciente. Este evento de error proporciona el código de error y una descripción de por qué se produjo un error en la implementación. Si un evento de error 465 precedió al evento 404, hubo un problema al abrir el paquete.

Si no se ha producido el error 465, consulte [solución de problemas generales de empaquetado, implementación y consulta de aplicaciones de Windows](troubleshooting.md). En caso contrario, consulte esta tabla para ver los códigos de error comunes que pueden aparecer en la cadena de error para el evento 465 de error:

| Código de error | Error                                 | Descripción                                                                                                          | Sugerencia                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | ERROR \_ al instalar el \_ \_ paquete abierto \_ | No se pudo abrir el paquete de la aplicación.                                                                                 | Este error suele indicar un problema con el paquete. Debe compilar y firmar el paquete de nuevo. Para obtener más información, vea [usar el Empaquetador de aplicaciones](make-appx-package--makeappx-exe-.md). |
| 0x80080205 | \_ \_ BLOCKMAP no válido de appx E \_            | El paquete de la aplicación se ha alterado o tiene una asignación de bloques no válida.                                                  | El paquete está dañado. Debe compilar y firmar el paquete de nuevo. Para obtener más información, vea [usar el Empaquetador de aplicaciones](make-appx-package--makeappx-exe-.md).                                  |
| 0x800B0004 | CONFIANZA \_ E \_ asunto \_ no de \_ confianza       | El paquete de la aplicación se ha alterado.                                                                              | El contenido del paquete ya no coincide con su firma digital. Debe volver a firmar el paquete. Para obtener más información, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md).  |
| 0x800B0100 | CONFIAR \_ E \_ nofirma                 | El paquete de la aplicación no tiene signo.                                                                                         | Solo se pueden implementar paquetes de aplicación de Windows firmados. Para obtener información sobre cómo firmar un paquete de la aplicación, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md).                  |
| 0x800B0109 | raíz de certificado \_ E no \_ confiable \_              | La cadena de certificados que se usó para firmar el paquete de aplicación termina en un certificado raíz que no es de confianza.           | Continúe con el paso 2 para solucionar los problemas de confianza de certificados.                                                                                                                                                  |
| 0x800B010A | encadenamiento de certificado \_ E \_                     | No se pudo compilar una cadena de certificados en una entidad de certificación raíz de confianza del certificado que se usó para firmar el paquete de la aplicación. | Continúe con el paso 2 para solucionar los problemas de confianza de certificados.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Paso 2: determinar la cadena de certificados usada para firmar el paquete de la aplicación

Para averiguar los certificados en los que el equipo local debe confiar, puede examinar la cadena de certificados de la firma digital en el paquete de la aplicación.

**Para determinar la cadena de certificados**

1.  En el explorador de archivos, haga clic con el botón derecho en el paquete de la aplicación y seleccione **propiedades**.
2.  En el cuadro de diálogo **propiedades** , seleccione la pestaña **firmas digitales** , que también muestra si se puede validar la firma.
3.  En la lista firma, seleccione la firma y, a continuación, haga clic en el botón **detalles** .
4.  En el cuadro de diálogo Detalles de la **firma digital** , haga clic en el botón **Ver certificado** .
5.  En el cuadro de diálogo **certificado** , seleccione la pestaña **ruta de certificación** .

El certificado superior de la cadena es el certificado raíz y el certificado inferior es el certificado de firma. Si solo hay un certificado en la cadena, el certificado de firma es también su propio certificado raíz. Puede determinar el número de serie de cada certificado que use después con [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)):

**Para determinar el número de serie de cada certificado**

1.  En el panel ruta de certificación, seleccione el certificado y, a continuación, haga clic en **Ver certificado**.
2.  En el cuadro de diálogo certificado, seleccione la pestaña **detalles** , que muestra el número de serie y otras propiedades útiles del certificado.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Paso 3: determinar los certificados de confianza del equipo local

Para poder implementar un paquete de la aplicación, no solo debe ser de confianza en el contexto del usuario sino también en el contexto del equipo local. Como resultado, la firma digital puede aparecer como válida cuando se ve en la pestaña firmas digitales del paso anterior, pero se sigue produciendo un error en la validación durante la implementación del paquete de la aplicación.

**Para determinar si la cadena de certificados usada para firmar el paquete de la aplicación es de confianza para el equipo local**

1.  Ejecute este comando:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Ejecute este comando:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Si no especifica el número de serie del certificado, [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) enumera todos los certificados en los que confía el equipo local para ese almacén.

Es posible que no se pueda instalar el paquete debido a errores de encadenamiento de certificados, incluso si el certificado de firma no es autofirmado y el certificado raíz está en el almacén raíz del equipo local. En este caso, puede haber un problema con la confianza para las entidades de certificación intermedias. Para obtener más información sobre este problema, consulte [trabajar con certificados](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Observaciones

Si ha determinado que el paquete no se pudo implementar porque el certificado de firma no es de confianza, no instale el paquete a menos que sepa dónde se originó y que confía en él.

Si quiere confiar manualmente en la aplicación para su instalación (por ejemplo, para instalar su propio paquete de aplicación firmado con prueba), puede Agregar manualmente el certificado a la confianza de certificado de equipo local desde el paquete de la aplicación.

**Para agregar manualmente el certificado al certificado de confianza del equipo local**

1.  En el explorador de archivos, haga clic con el botón derecho en el paquete de la aplicación y, en el menú contextual emergente, seleccione **propiedades**.
2.  En el cuadro de diálogo **propiedades** , seleccione la pestaña **firmas digitales** .
3.  En la lista firma, seleccione la firma y, a continuación, haga clic en el botón **detalles** .
4.  En el cuadro de diálogo Detalles de la **firma digital** , haga clic en el botón **Ver certificado** .
5.  En el cuadro de diálogo **certificado** , haga clic en **instalar certificado..** . .
6.  En el Asistente para importación de certificados, seleccione **equipo local** y, a continuación, haga clic en **siguiente**. Tendrá que conceder privilegios de administrador para continuar.
7.  Seleccione **colocar todos los certificados en el siguiente almacén** y vaya al almacén de **usuarios de confianza** .
8.  Haga clic en **siguiente** y, a continuación, haga clic en **Finalizar** para completar el asistente.

Después de esta adición manual, puede ver que el certificado ahora es de confianza en el cuadro de diálogo **certificado** .

Puede quitar el certificado después de que ya no lo necesite.

**Para quitar el certificado**

1.  Ejecute **Cmd.exe** como administrador.
2.  En el símbolo del sistema de administrador, ejecute este comando:

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Busque el número de serie del certificado que instaló. Este número es el *certID*.
4.  Ejecute este comando:

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

Le recomendamos que evite agregar manualmente los certificados raíz al almacén de [certificados de entidades de certificación raíz de confianza](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)del equipo local. Tener varias aplicaciones firmadas con certificados que encadenan al mismo certificado raíz, como aplicaciones de línea de negocio, puede ser más eficaz que la instalación de certificados individuales en el almacén de usuarios de confianza. El almacén de personas de confianza contiene certificados que se consideran de confianza de forma predeterminada, por lo que no se comprueban por entidades o listas de confianza de certificados o entidades superiores. Para obtener consideraciones sobre cómo agregar certificados al almacén de certificados de entidades de certificación raíz de confianza, vea [procedimientos recomendados para la firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85)).

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Al agregar un certificado a los [almacenes de certificados del equipo local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), afecta a la confianza del certificado de todos los usuarios del equipo. Se recomienda instalar los certificados de firma de código que desee para probar paquetes de aplicaciones en el almacén de certificados de personas de confianza. Quite los certificados inmediatamente cuando ya no sean necesarios, para evitar que se usen para poner en peligro la confianza del sistema. Si crea sus propios certificados de prueba para firmar paquetes de aplicaciones, también se recomienda restringir los privilegios asociados al certificado de prueba. Para obtener información sobre cómo crear certificados de prueba para firmar paquetes de aplicaciones, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Ejemplos**
</dt> <dt>

[Crear paquete de aplicación ejemplo]https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceptos**
</dt> <dt>

[Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows](troubleshooting.md)
</dt> <dt>

[Tareas certutil para administrar certificados](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 